# `pendulum_sample.csv`: Provenance

## Source
Synthetic dataset for HW0 (Module 1, Pendulum Gravity). Not an external dataset: produced by `scripts/generate_pendulum_data.py` with a fixed RNG seed.

## License
Instructor-created course material (GEOL 333 / 714, Fall 2026). No external license or attribution constraint; free to post and redistribute as course content.

## Generating model
- Physics: `T = 2π·sqrt(l/g)`, with `g_true = 9.81 m/s²` (the value the data is generated from).
- Noise: a phone-stopwatch start/stop error of about 0.15 s on the 10-swing measurement, divided by the 10 swings, gives `σ_T = 0.015 s` per derived single-period value; Gaussian noise at that σ is added to each period. Stacking 10 swings is 10× cleaner than single-swing timing, which is the point of the protocol.
- Protocol (locked 2026-06-12, eval step 5): each trial times 10 complete swings and divides by 10; amplitude stays under 15°.
- Sampling: 5 lengths (0.40, 0.60, 0.80, 1.00, 1.20 m), 5 trials each = 25 rows.
- Seed: `SEED = 333` (deterministic; re-running reproduces this file byte-for-byte).

## Columns
| name | unit | description |
|---|---|---|
| `trial` | integer | trial index, 1 to 25 |
| `length_m` | m | pendulum length for the trial (one of the 5 lengths). **True length, pivot to the center of the bob** (convention ruled 2026-09-04, rulings 16-17): on the classroom apparatus the string is marked at `l − 1.27 cm`, so the mark sits at the top of the one-inch bob and the center sits at `l`. The synthetic lengths carry no built-in offset. |
| `period_s` | s | observed single-swing period (10-swing time ÷ 10), rounded to 4 decimals |

The Wk 2 in-class file `pendulum_inclass.csv` uses the same length convention with two more
columns (`station,trial,length_m,t10_s,period_s`); see `pendulum_inclass_PROVENANCE.md`.

## Expected results (for grading; see `rubric_hw0.md`)
- Least-squares `T²` vs `l` slope positive, about +4.0 to +4.2 s²/m (slope = `4π²/g`).
- Recovered `g ≈ 9.66 m/s²`, about 1.5% below the 9.81 used to generate it. That gap is the intended discussion point in HW0 Part 6, not an error.
- The generator prints the exact recovered g, slope, and intercept as a sanity check on each run.

## Reproducibility
`scripts/generate_pendulum_data.py` regenerates this CSV deterministically (seed 333). Run with `uv run --with numpy --with pandas python scripts/generate_pendulum_data.py`.
