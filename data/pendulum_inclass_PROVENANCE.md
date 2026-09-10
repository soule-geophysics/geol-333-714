# `pendulum_inclass.csv`: Provenance

## Source
Collected by the GEOL 333/714 class on **Wednesday 9 September 2026** in the D237 lab, at five
pendulum stations running in parallel. Each station recorded its own timings on paper. This CSV is
a transcription of those sheets, made 10 September 2026. **The paper sheets are the original**; the
CSV is the readable copy.

## License
Instructor- and class-created course data (GEOL 333/714, Fall 2026). No external license or
attribution constraint; free to post and redistribute as course content.

## Protocol
Five stations, each running the full protocol at its own apparatus: five lengths, five trials per
length, each trial timing **ten complete swings and dividing by ten**, amplitude under 15°.

**Length convention.** `length_m` is the true pendulum length, pivot to the **centre** of the bob.
Strings are marked at `l − 1.27 cm`, so the mark sits at the top of the one-inch bob and the reader
adds the bob's radius. The five mark targets are 40.3, 60.5, 79.8, 100.6 and 119.4 cm from the top
of the bob, which makes the true lengths **0.4157, 0.6177, 0.8107, 1.0187 and 1.2067 m**.

125 rows: 5 stations × 5 lengths × 5 trials. All present.

## Columns
| name | unit | description |
|---|---|---|
| `station` | label | apparatus identifier, `A` to `E` (text; identifies a ringstand, never a person) |
| `trial` | integer | trial index, 1 to 5, within each station and length |
| `length_m` | m | true pendulum length, pivot to centre of bob (one of the five set lengths) |
| `t10_s` | s | raw stopwatch time for ten complete swings |
| `period_s` | s | derived single-swing period, `t10_s / 10` |

Periods are given to three decimals, which is the exact result of dividing a hundredth-of-a-second
stopwatch reading by ten. Further digits would be precision the instrument never had; the spread
across trials is what carries the uncertainty.

## Editing
**None.** Every value is as recorded on the paper sheets.

## Expected results (for grading; see `rubric_hw0.md`)
The rubric's in-class column applies: no fixed numerical target beyond a positive recovered `g`,
with units and an uncertainty, compared against 9.81 m/s². With 125 rows the per-length stacks are
N = 25. The result of a run is whatever the data say, plus its error bar.

## Reproducibility
Transcribed by `scripts/build_pendulum_inclass.py` in the course build repository and validated by
`scripts/check_pendulum_inclass.py`, which checks structure, arithmetic (`period_s` equals
`t10_s / 10`) and physics (each period against `T = 2π√(l/g)`, reported as a row to re-read rather
than as an error, since real scatter is expected).

Posted to `soule-geophysics/geol-333-714/data/pendulum_inclass.csv` and linked from the Brightspace
Week 2 page.
