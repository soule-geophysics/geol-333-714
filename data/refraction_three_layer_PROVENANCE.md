# `refraction_three_layer.csv`: Provenance

## Source
**Synthetic.** This dataset is generated, not measured. It supports the three-layer half of HW5b (Burger §3.3 and §3.4). It carries no external license constraint and is fully reproducible from the script.

## Generator
`scripts/generate_refraction_data.py` (`build_three_layer`). Regenerate all three HW5 files with:

```
uv run python scripts/generate_refraction_data.py
```

The generator prints a self-recovery check for each file.

## Seed
`SEED = 333` (the project convention). `numpy.random.default_rng(333)` draws one noise value per geophone in offset order. The CSV is bit-for-bit reproducible from this seed. The seed was not changed after looking at the draw (see the recovery table).

## Columns
| name | unit | description |
|---|---|---|
| `offset_m` | m | geophone offset from the source (2 to 96 m, 2 m spacing) |
| `first_break_ms` | ms | picked first-arrival time, milliseconds |
| `travel_time_s` | s | the same time in seconds; the column HW5 fits |

48 rows, one forward spread.
