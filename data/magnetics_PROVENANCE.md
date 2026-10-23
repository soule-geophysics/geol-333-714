# `magnetics.csv`: Provenance

## Source
**Synthetic.** This dataset is generated, not measured. It is the guaranteed HW4 dataset (Diurnal Correction and the Magnetic Residual). It carries no external license constraint: it is fully reproducible from the script, like `refraction.csv` and `pendulum_sample.csv`. The site is a hypothetical survey line at the latitude of the Queens College campus; no survey was run there.

## Generator
`scripts/generate_magnetics_data.py`. Regenerate with:

```
uv run python scripts/generate_magnetics_data.py
```

The generator prints a preview and a self-recovery check: it runs the diurnal, IGRF and regional reductions on the CSV and compares the residual to the true anomaly.

## Seed
`SEED = 333` (the project convention, matching `generate_pendulum_data.py` and `generate_refraction_data.py`). The CSV is bit-for-bit reproducible from this seed. The seed sets the three pulsation phases and the rover and base noise draws; every other quantity is deterministic.

## Physics
One ground total-field profile, walked with a rover magnetometer while a second magnetometer logs at a fixed base station on the same clock:

$$F_\text{rover}(x, t) = F_\text{IGRF}(x) + F_\text{reg}(x) + \Delta T(x) + D(t) + \varepsilon_r$$

$$F_\text{base}(t) = F_\text{IGRF}(x_b) + F_\text{reg}(x_b) + \Delta T(x_b) + D(t) + \varepsilon_b$$

- $F_\text{IGRF}(x)$: the main field from IGRF-14, supplied per station in `igrf_nT`.
- $F_\text{reg}(x)$: a linear regional anomaly from deep crustal sources, which IGRF does not contain. Not supplied; the student fits it.
- $\Delta T(x)$: the target, the total-field anomaly of a buried sphere with induced magnetization.
- $D(t)$: the external field, a solar-quiet (Sq) daily variation plus quiet-day Pc5 pulsations. It is identical at rover and base, since the sensors are a few hundred meters apart and the external current systems are hundreds of kilometers across.
- $\varepsilon_r, \varepsilon_b$: independent Gaussian instrument noise.

**Target.** A sphere of radius $a$ with susceptibility $\chi$, magnetized by the main field only (no remanence). Its external field is exactly that of a point dipole at its center with moment

$$m = \frac{\chi}{1 + \chi/3}\,\frac{F}{\mu_0}\,\frac{4}{3}\pi a^3,$$

which includes the exact self-demagnetization factor for a sphere. The moment points along the main field, $\hat{\mathbf{f}} = (\cos I, 0, \sin I)$ in (magnetic north, east, down). The total-field anomaly is the projection of the dipole field on $\hat{\mathbf{f}}$ (valid because $|\Delta T| \ll F$):

$$\Delta T = \frac{\mu_0 m}{4\pi r^3}\left[3(\hat{\mathbf{f}}\cdot\hat{\mathbf{r}})^2 - 1\right].$$

The line runs along the magnetic meridian (azimuth = declination), distance increasing to magnetic north, so the inducing field lies in the vertical plane of the profile. At $I = 65.5°$ the positive peak sits south of the source and a negative lobe lies to the north.

**External field.**

$$D(t) = A_{24}\cos\frac{2\pi(t - t_0)}{24\,\text{h}} + A_{12}\cos\frac{2\pi(t - t_0)}{12\,\text{h}} + \sum_{k=1}^{3} a_k \sin\left(\frac{2\pi t}{P_k} + \phi_k\right)$$

with $t_0$ at local apparent solar noon and $\phi_k$ drawn from the seed.

**Diurnal correction** (the step HW4 Part 2 performs):

$$F_\text{dc} = F_\text{rover} - \left(F_\text{base} - F_\text{base}^{(0)}\right),$$

where $F_\text{base}^{(0)}$ is the first base reading. This removes $D(t)$ exactly and leaves the rover and base noise in quadrature, $\sqrt{0.5^2 + 0.2^2} = 0.54$ nT, plus a constant offset that the regional fit absorbs.

## True input parameters (constants in the generator)

**Site and main field.** IGRF-14 values computed once with the `ppigrf` package (v2.1.0) for 2026-10-10 at 30 m elevation, along the line at 100 m intervals, then frozen as constants.

| symbol | value | justification |
|---|---|---|
| site | 40.7360° N, 73.8170° W | hypothetical line at the Queens College campus latitude |
| survey date | 2026-10-10 (quiet day assumed) | inside the teaching term; IGRF-14 epoch valid 2025-2030 |
| `IGRF_F0_NT` | 50742.7 nT | IGRF-14 total field at station 0 |
| `IGRF_GRADIENT_NT_PER_M` | 0.00496 nT/m (4.96 nT/km, rising north) | IGRF-14 at 0 m and 400 m: 50742.69 and 50744.68 nT; linear to 0.01 nT |
| `IGRF_INCLINATION_DEG` | 65.50° | IGRF-14; varies by < 0.01° along the line |
| `IGRF_DECLINATION_DEG` | −12.55° | IGRF-14; the line azimuth |

**Profile and timing.**

| symbol | value | justification |
|---|---|---|
| `LINE_LENGTH_M` | 400 m | the anomaly falls below 1 nT beyond ~120 m from the source; leaves ~120 m of flank to the south and ~50 m to the north for the regional fit |
| `STATION_SPACING_M` | 5 m (81 stations) | about five samples per source depth (26 m below sensor); resolves the peak and its half-width |
| `SENSOR_HEIGHT_M` | 2 m | standard staff height for a walked proton-precession or Overhauser survey; lifts the sensor above small near-surface iron |
| `SURVEY_START` | 08:30 EDT | the morning limb of Sq, when the external field changes fastest on a quiet day |
| `SECONDS_PER_STATION` | 90 s | 1-3 s per reading cycle; the occupation covers three repeat readings, logging, a 5 m walk and re-plumbing the staff. 81 stations span 08:30-10:30 |
| `BASE_OFFSET_WEST_M` | 150 m west of station 0 | far enough that the target contributes < 0.05 nT at the base (computed: −0.02 nT) |

**External field.**

| symbol | value | justification |
|---|---|---|
| `DIURNAL_A24_NT`, `DIURNAL_A12_NT` | −20 nT, −10 nT | first two solar-day harmonics; 30 nT daily range, inside the 20-50 nT quiet-day range for mid-latitude total field; negative signs put the daytime minimum at $t_0$ |
| periods | 24 h, 12 h | the solar day and its first harmonic |
| `DIURNAL_T0_HOURS` | 12:42 EDT | local apparent solar noon at 73.82° W on 10 Oct: mean noon 16:55 UTC (12:55 EDT), minus the ~13 min equation of time |
| `PULSATION_AMPLITUDES_NT` | 1.0, 0.7, 0.5 nT | quiet-day Pc5 pulsations, a few nT at most |
| `PULSATION_PERIODS_MIN` | 4.0, 6.5, 9.0 min | inside the Pc5 band (150-600 s) |

Over the survey the Sq term falls by 17.7 nT and the full external field spans 18.6 nT.

**Regional field.**

| symbol | value | justification |
|---|---|---|
| `REGIONAL_GRADIENT_NT_PER_M` | 0.040 nT/m (40 nT/km, rising north) | ground-survey regional gradients over crystalline basement run from a few to ~100 nT/km; 40 nT/km tilts the residual visibly if Part 4 is skipped (16 nT across the line) |
| `REGIONAL_LEVEL_NT` | +35 nT at 200 m | a broad positive regional, so the total-field anomaly is offset from zero |

**Target.**

| symbol | value | justification |
|---|---|---|
| geometry | sphere (uniformly magnetized) | exact dipole field outside the body; the Module 2 anchor equation |
| `SOURCE_X_M` | 230 m (station 46) | off-center, so the peak location is a measurement |
| `SOURCE_DEPTH_BELOW_GROUND_M` | 24 m to center (26 m below sensor) | shallow enough for a 5 m station spacing to resolve; deep enough that the anomaly is broad compared to near-surface noise |
| `SOURCE_RADIUS_M` | 10 m | a small mafic body or plug |
| `SOURCE_SUSCEPTIBILITY_SI` | 0.05 SI | inside the tabulated range for diabase (~0.001-0.16 SI); host (gneiss / glacial sediment, ~1e-4 SI) treated as non-magnetic, so 0.05 is the contrast |
| magnetization | induced only | HW4 Part 6 names remanence as what a total-field survey cannot separate |

Derived: moment $m = 8.32 \times 10^3$ A m²; peak anomaly +82.4 nT at 224.3 m (5.7 m south of the source); northern low −10.6 nT at 256.3 m; full width at half maximum 26.3 m.

**Noise.**

| symbol | value | justification |
|---|---|---|
| `SIGMA_ROVER_NT` | 0.5 nT (1σ) | sensor sensitivity is 0.01-0.1 nT; a walked sensor adds staff-height, tilt and heading error, and 0.5 nT is a conservative field repeatability |
| `SIGMA_BASE_NT` | 0.2 nT (1σ) | fixed sensor, no positioning error |
| `READING_RESOLUTION_NT` | 0.1 nT | display resolution of a proton-precession unit; readings are rounded to it |
| `SEED` | 333 | project convention |

## Columns
| name | unit | description |
|---|---|---|
| `station` | none | station number, 0 at the south end to 80 at the north end |
| `distance_m` | m | distance along the line from station 0, magnetic north positive (0 to 400 m, 5 m spacing) |
| `time` | ISO 8601 | local clock time of the reading (EDT, UTC−4), e.g. `2026-10-10T08:30:00` |
| `elapsed_min` | min | minutes since the first rover reading (0 to 120, 1.5 min steps) |
| `rover_nT` | nT | rover total-field reading at the station |
| `base_nT` | nT | base-station total-field reading at the same clock time |
| `igrf_nT` | nT | IGRF-14 main field at the station |

81 rows, one line. `time` and `elapsed_min` carry the same clock in two forms: `time` is what a field logger records, `elapsed_min` plots directly.

## Self-recovery check (from the generated CSV)
Reductions as HW4 runs them: diurnal correction by base subtraction, IGRF subtraction, a straight-line regional fitted with `polyfit(cov=True)` to stations more than 100 m from the anomaly peak (40 stations), residual = anomaly − regional.

| quantity | recovered | true |
|---|---|---|
| diurnal-corrected error, std | 0.62 nT | 0.54 nT expected (rover and base in quadrature) |
| rover error with no base correction, std | 5.35 nT | (the external field left in) |
| regional gradient | 39.3 ± 0.6 nT/km | 40.0 nT/km |
| residual − true anomaly | rms 0.62 nT, max 1.58 nT | 0 |
| residual peak | 82.4 nT at 225 m (± 2.5 m, half a station) | 82.4 nT at 224.3 m |
| residual full width at half maximum | 26.1 m | 26.3 m |

The diurnal-corrected scatter (0.62 nT) is 1.9 standard errors above the expected 0.54 nT (standard error of a sample std with n = 81 is ~0.04 nT); it is the draw for seed 333. The regional gradient recovers within 1.1σ; the ~0.7 nT/km low bias comes from the dipole tails that remain inside the fitting window. Without the base correction the profile error is about 9 times larger, so the diurnal step is necessary to see the target's flanks and its northern low.

The residual peak lies 5 m south of the source (230 m). The offset is the inclination effect: for the same body at the pole ($I = 90°$) the peak sits over the source. This is the shift that reduction to the pole removes. For a vertically magnetized sphere the vertical-field half-width gives depth as $z \approx 2\,x_{1/2}$; the residual's half-width of 13 m gives 26 m, the true depth below the sensor. At $I = 65.5°$ the rule is approximate, and it holds here within one station spacing.

## How HW4 uses it
HW4 loads this CSV through a single `DATA_URL` / `FILENAME` variable. The dataset supports:

1. loading and inspecting the survey (`.head`, `.describe`);
2. plotting the base record against time and subtracting the time-matched base reading (diurnal correction);
3. subtracting `igrf_nT` to form the total-field anomaly;
4. fitting and removing a straight-line regional with `numpy.polyfit`;
5. locating the residual peak and northern low, estimating depth from the half-width, and naming the south shift of the peak that reduction to the pole would remove;
6. stating what the survey cannot resolve: remanence, and the trade-off between susceptibility and volume.

If the IGUaNA Unit 3 magnetics data is cleared for use, a real CSV replaces this one by re-pointing the one `DATA_URL` line; the self-check values above are pinned to this synthetic CSV.
