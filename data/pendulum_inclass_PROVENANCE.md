# `pendulum_inclass.csv`: Provenance

> **Drafted in advance 2026-09-04** (schema ruled that day, rulings 16-17 in
> `docs/lesson_plans/records/rulings_2026_09_04.md`; the schema doc's §6 asks for this sidecar
> to exist before the file does). The file itself is written in class on **Wed Sep 9, 2026**
> and posted that evening. Fields marked FILL are completed at posting.

## Source
Collected live by the GEOL 333/714 class at five pendulum stations in the D237 lab, Queens
College CUNY, Wed Sep 9, 2026, following the Pendulum Data Collection Sheet. Typed into the
file by the instructor as readings are called; exported during the class break. FILL: number
of students present, any station anomalies.

## License
Instructor- and class-created course data (GEOL 333/714, Fall 2026). No external license or
attribution constraint; free to post and redistribute as course content. Contains no student
names or identifiers: `station` is an apparatus label, never a person or group of people.

## Protocol
Five stations, each running the full protocol at its own apparatus: five true lengths
(0.400, 0.600, 0.800, 1.000, 1.200 m), five trials per length, each trial timing ten complete
swings and dividing by ten, amplitude under 15°. **Length convention (ruled 2026-09-04):**
`length_m` is the true pendulum length, pivot to the center of the bob; strings are marked at
`l − 1.27 cm` so the mark sits at the top of the one-inch bob. 125 rows expected. FILL:
actual row count and any deviations.

## Columns
| name | unit | description |
|---|---|---|
| `station` | label | apparatus identifier, `A` to `E` (text; identifies a ringstand, never a person) |
| `trial` | integer | trial index, 1 to 5, within each station-and-length |
| `length_m` | m | true pendulum length, pivot to center of bob (one of the 5 set lengths) |
| `t10_s` | s | raw stopwatch time for 10 complete swings |
| `period_s` | s | derived single-swing period, `t10_s / 10` |

## Expected results (for grading; see `rubric_hw0.md`)
The rubric's in-class column applies: no fixed numerical target beyond a positive recovered g,
with units, compared against 9.81 m/s². With 125 rows the per-length stacks are N = 25, so
standard errors run about 1/√5 of the sample CSV's and the fitted σ_g lands near 0.04 m/s²
if per-trial scatter matches the sample's. FILL: the actual fitted slope, intercept, and g ± σ
after collection.

## Reproducibility
Primary record: this CSV plus the paper collection sheets (each sheet carries its station
letter). The file posts to three places the same evening: `outputs/data/` (this repo), the
public course-data mirror `soule-geophysics/geol-333-714/data/pendulum_inclass.csv`, and the
Brightspace Wk 2 page. FILL: the publish commit hashes.
