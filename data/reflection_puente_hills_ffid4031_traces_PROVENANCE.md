# `reflection_puente_hills_ffid4031_traces.csv`: Provenance

## Source

**Real field data.** The recorded traces of one sledgehammer shot on a shallow seismic reflection line along Carfax Avenue, Los Angeles, California, across the Puente Hills fault zone, acquired by the U.S. Geological Survey in April 2000. The same shot gives the reflection picks in `reflection_puente_hills_ffid4031.csv`.

> Pratt, T.L., 2026, Seismic reflection profiles across the Puente Hills fault zone, Los Angeles, California: U.S. Geological Survey data release, https://doi.org/10.5066/P1XIR92T.

- Release: https://doi.org/10.5066/P1XIR92T (ScienceBase item 68dac499d4be021b36eb644f)
- Archive: `Carfax_hammer.zip` (211 MB), retrieved 2026-11-07, SHA-256 `f46bc32765c39ff6223bf0e86857758a99d3234a218cf4bc18df11abcaba5820`
- File used: `Carfax_hammer/shots_w_geom2.sgy` (107 MB, geometry in the trace headers, 4-byte IBM float), SHA-256 `c80eec0ed0208b7222c6ba123f30b2a325ce4463ac151c388c599863d740bfbb`
- Acquisition (`acquisition_parameters.txt` in the release): sledgehammer, 2 hits per station, 60 channels, 1 m geophone and shot spacing, source at geophone 1 (end-on spread, offsets 0 to 59 m), 0.5 ms sampling, 0.5 s records.

Record used: field file 4031, source at x = 116 m on the profile.

## License

The release metadata (`useconst`, retrieved 2026-11-07) reads: "These data are marked with a Creative Commons Zero v1.0 Universal (CC0-1.0) public domain dedication and do not have any use constraints." Credit: U.S. Geological Survey, Pratt (2026).

## Columns

| Column | Unit | Meaning |
|---|---|---|
| `time_ms` | ms | Time after the hammer blow, 0 to 200 ms in 0.5 ms steps (401 rows) |
| `6` ... `59` | none | One column per live geophone, named by its offset from the source in meters: the band-passed ground motion in SEG-Y amplitude units (digitizer counts after filtering), unscaled |

46 trace columns, offsets 6 to 59 m. The 11 dead traces (offsets 3, 4, 5, 19, 20, 33, 34, 35, 49, 50 and 52 m) are left out, as are offsets 0 to 2 m. File size 112 KB. SHA-256 of this CSV: `25a3142cc270ef68d8a48c9b0036f09e471b923a617b508e0e3f89fef34adee5`.

## Reproducibility: processing

Script: `scripts/trim_puente_hills_gather.py`. Tests: `tests/test_trim_puente_hills_gather.py`.

1. Read the 60 traces of field file 4031 from `shots_w_geom2.sgy`, sorted by the offset header.
2. Dead-trace rule (the rule of the reflection picks): a trace is dead if its RMS amplitude over the full 0.5 s record is under 10 percent of the shot median. Dead traces are dropped.
3. Band-pass 60 to 300 Hz, 4-pole Butterworth, zero phase (`scipy.signal.sosfiltfilt`), on the full record. This is the band the reflection picks were made in, so each pick sits on the peak it was made on.
4. Keep offsets of 6 m or more and samples from 0 to 200 ms. The picks start at 6 m and end at 181 ms.
5. Gain and scaling: none. The values keep the SEG-Y amplitude units, so the relative amplitudes between traces are true (largest absolute value about 1.0e5 near the source, about 1.7e2 at 59 m). Values rounded to 1 decimal. Revised 2026-11-17 (ruling E10): the first version scaled each trace to a peak of 1, which hid the amplitude decay with offset and made one display gain impossible.

```
uv run --with segyio --with scipy python scripts/trim_puente_hills_gather.py
```

The SEG-Y must sit under `outputs/data/raw/puente_hills_carfax_hammer/` (gitignored).

## Retired: the HW5a first-break figure

From 2026-11-17 (ruling E7) until later the same day (ruling E8), HW5a showed a first-break figure drawn from this CSV. This record is a reflection survey and shows no head wave, so ruling E8 replaced that figure with a synthetic gather computed from the HW5a two-layer model (`scripts/build_hw5a_synthetic_gather_figure.py`). This CSV now serves HW5c only.
