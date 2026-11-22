# `pendulum_sample.csv`: Provenance

## Source
Synthetic dataset for HW0 (Module 1, Pendulum Gravity). Not an external dataset: produced by `generate_pendulum_data.py` with a fixed RNG seed.

`generate_pendulum_data.py` is in the course build repository, not published here.

## License
Instructor-created course material (GEOL 333 / 714, Fall 2026). No external license or attribution constraint; free to post and redistribute as course content. Instructor-created course data, released under CC BY 4.0 with the rest of this repository.

## Columns
| name | unit | description |
|---|---|---|
| `trial` | integer | trial index, 1 to 25 |
| `length_m` | m | pendulum length for the trial (one of the 5 lengths). **True length, pivot to the center of the bob** (convention ruled 2026-09-04, rulings 16-17): on the classroom apparatus the string is marked at `l − 1.27 cm`, so the mark sits at the top of the one-inch bob and the center sits at `l`. The synthetic lengths carry no built-in offset. |
| `period_s` | s | observed single-swing period (10-swing time ÷ 10), rounded to 4 decimals |

The Wk 2 in-class file `pendulum_inclass.csv` uses the same length convention with two more
columns (`station,trial,length_m,t10_s,period_s`); see `pendulum_inclass_PROVENANCE.md`.

## Reproducibility
`generate_pendulum_data.py` regenerates this CSV deterministically (seed 333).

`generate_pendulum_data.py` is in the course build repository, not published here.
