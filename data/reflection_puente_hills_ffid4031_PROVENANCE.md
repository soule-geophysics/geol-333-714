# `reflection_puente_hills_ffid4031.csv`: Provenance

## Source

**Real field data.** Reflection-time picks from one sledgehammer shot on a shallow seismic reflection line along Carfax Avenue, Los Angeles, California, across the Puente Hills fault zone, acquired by the U.S. Geological Survey in April 2000.

> Pratt, T.L., 2026, Seismic reflection profiles across the Puente Hills fault zone, Los Angeles, California: U.S. Geological Survey data release, https://doi.org/10.5066/P1XIR92T.

- Release: https://doi.org/10.5066/P1XIR92T (ScienceBase item 68dac499d4be021b36eb644f)
- Data credit (release metadata): James Dolan, University of Southern California; John Shaw, Harvard University.
- Archive: `Carfax_hammer.zip` (211 MB), retrieved 2026-11-07; file used `Carfax_hammer/shots_w_geom2.sgy` (geometry in the trace headers)
- Acquisition (`acquisition_parameters.txt` in the release): sledgehammer, 2 hits per station, 60 channels, 1 m geophone and shot spacing, source at geophone 1 (end-on spread, offsets 0 to 59 m), 0.5 ms sampling, 0.5 s records.

Record used: field file 4031, source at x = 116 m on the profile. The picks were made by the course instructor from the public record. They are not part of the release.

## License

The release metadata (`useconst`, retrieved 2026-11-07) reads: "These data are marked with a Creative Commons Zero v1.0 Universal (CC0-1.0) public domain dedication and do not have any use constraints." Credit: U.S. Geological Survey, Pratt (2026).

## Columns

| Column | Unit | Meaning |
|---|---|---|
| `offset_m` | m | Distance from the source to the geophone along the line |
| `reflection_time_ms` | ms | Picked two-way reflection time |
| `travel_time_s` | s | `reflection_time_ms` / 1000 |

43 rows, offsets 6 to 59 m. Geophones are 1 m apart. Gaps of up to 4 m occur where a trace was dead or carried no clear peak (see the extraction steps).

## Reproducibility: extraction

Scripts: `scripts/puente_hills_reflection_picks.py` (picks) and `scripts/extract_puente_hills_reflection.py` (this file). Tests: `tests/test_puente_hills_reflection_fit.py`, `tests/test_extract_puente_hills_reflection.py`.

1. Read the 60 traces of field file 4031 from `shots_w_geom2.sgy`, sorted by offset.
2. Dead-trace rule, set before any fit: a trace is dead if its RMS amplitude is under 10 percent of the shot median. Eleven traces fail (offsets 3, 4, 5, 19, 20, 33, 34, 35, 49, 50 and 52 m).
3. Band-pass 60 to 300 Hz (4-pole Butterworth, zero phase). A 30 ms AGC is applied for the semblance scan and display only.
4. Semblance scan of the live traces at offsets of 3 m or more, t0 40 to 80 ms and V 200 to 800 m/s. Maximum at t0 = 58.5 ms, V = 344 m/s.
5. On each trace, the positive peak of the filtered (not AGC) trace within ±3 ms of that hyperbola, with parabolic sub-sample interpolation. A trace whose peak falls on the window edge has no clear peak and is excluded. Offsets under 3 m are excluded because the source wavetrain overlaps the event there.
6. Keep the picks that pass steps 2 and 5 (`used_in_fit = 1` in `puente_hills_carfax_ffid4031_reflection_picks.csv`, which lists every pick with its exclusion reason). Times rounded to 0.01 ms.

No pick was edited or removed for fit quality.

## Reproducibility: rerun

```
uv run --with segyio --with scipy --with matplotlib python scripts/puente_hills_reflection_picks.py 4031
uv run python scripts/extract_puente_hills_reflection.py
```

The first step needs the SEG-Y under `outputs/data/raw/puente_hills_carfax_hammer/` (gitignored). The second runs from the committed picks file alone.
