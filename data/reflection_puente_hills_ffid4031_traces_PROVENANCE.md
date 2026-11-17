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
| `6` ... `59` | none | One column per live geophone, named by its offset from the source in meters: the band-passed ground motion, scaled so the largest absolute value in the column is 1 |

46 trace columns, offsets 6 to 59 m. The 11 dead traces (offsets 3, 4, 5, 19, 20, 33, 34, 35, 49, 50 and 52 m) are left out, as are offsets 0 to 2 m. File size 138 KB. SHA-256 of this CSV: `7dcd0bcff450d647eb536a26dfebec432b139afd0fbe8633ebf3fe9535ee44e6`.

## Reproducibility: processing

Script: `scripts/trim_puente_hills_gather.py`. Tests: `tests/test_trim_puente_hills_gather.py`.

1. Read the 60 traces of field file 4031 from `shots_w_geom2.sgy`, sorted by the offset header.
2. Dead-trace rule (the rule of the reflection picks): a trace is dead if its RMS amplitude over the full 0.5 s record is under 10 percent of the shot median. Dead traces are dropped.
3. Band-pass 60 to 300 Hz, 4-pole Butterworth, zero phase (`scipy.signal.sosfiltfilt`), on the full record. This is the band the reflection picks were made in, so each pick sits on the peak it was made on.
4. Keep offsets of 6 m or more and samples from 0 to 200 ms. The picks start at 6 m and end at 181 ms.
5. Gain: none in time. Each trace is divided by its largest absolute value in the 0 to 200 ms window, so every column peaks at 1 and the traces can be drawn side by side. Relative amplitudes between traces are not kept. Values rounded to 4 decimals.

```
uv run --with segyio --with scipy python scripts/trim_puente_hills_gather.py
```

The SEG-Y must sit under `outputs/data/raw/puente_hills_carfax_hammer/` (gitignored).

## Reproducibility: the HW5a first-break figure

`outputs/figures/geol333_hw5a_ffid4031_first_breaks.png` (published as `figures/geol333_hw5a_ffid4031_first_breaks.png`) is drawn from this CSV by `scripts/build_hw5a_first_break_figure.py`. The first-break marks are for illustration only; no number from them enters a calculation or an answer.

- Search guide: the earliest coherent arrival on traces 21 to 48 m lines up with a straight line through the origin at about 343 m/s.
- Noise level per trace: RMS amplitude from 20 to 10 ms before the guide time.
- First break: the first sample from 10 ms before to 10 ms after the guide time whose absolute amplitude reaches 6 times the noise level. A trace with no such sample gets no mark.
- Result: 33 of the 46 traces marked, from 18.5 ms at 6 m to 155.0 ms at 51 m. Unmarked: 8, 9, 10, 12, 40, 47 and 53 to 59 m.
- Display: each trace multiplied by 1.5 and clipped at 0.6, so the weak first motion shows next to the stronger later arrivals. Traces 1 m apart.

```
uv run python scripts/build_hw5a_first_break_figure.py
```
