# `refraction.csv`: Provenance

## Source
**Synthetic.** This dataset is generated, not measured. It supports HW5a and the two-layer half of HW5b (rulings of 2026-11-05 and 2026-11-06). It carries no external license constraint and no `{{INSTRUCTOR VERIFIES}}` flag: it is fully reproducible from the script, exactly like `pendulum_sample.csv`.

## Generator
`scripts/generate_refraction_data.py`. Regenerate with:

```
uv run python scripts/generate_refraction_data.py
```

The generator prints a preview and a self-recovery sanity check (recovers v1, v2, crossover, and depth from the picked travel times and compares them to the true inputs).

## Seed
`SEED = 333` (the project convention, matching `generate_pendulum_data.py`). The CSV is bit-for-bit reproducible from this seed.

## Columns
| name | unit | description |
|---|---|---|
| `offset_m` | m | geophone offset from the source (3 to 72 m, 3 m spacing) |
| `first_break_ms` | ms | picked first-arrival time, milliseconds (= 1000 × `travel_time_s`) |
| `travel_time_s` | s | the same first-arrival time in seconds; the SI column HW5 fits |

`first_break_ms` and `travel_time_s` carry the same measurement in two units. HW5 fits `travel_time_s` (so the slope comes out in s/m and `1/slope` is directly m/s); `first_break_ms` is provided because field seismographs report first breaks in milliseconds.

24 rows, one forward spread. The same script also writes `refraction_three_layer.csv` and `reflection_one_layer.csv` (HW5b and HW5c), each with its own provenance file; generating them did not change this file. The arc rulings of 2026-11-05 exclude dipping layers and reversed spreads, so no reversed file is made.
