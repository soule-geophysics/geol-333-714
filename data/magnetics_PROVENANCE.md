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
