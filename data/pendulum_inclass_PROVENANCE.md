# `pendulum_inclass.csv`: Provenance

> **Drafted in advance 2026-09-04** (schema ruled that day, rulings 16-17 in
> `docs/lesson_plans/records/rulings_2026_09_04.md`; the schema doc's §6 asks for this sidecar
> to exist before the file does). The file itself is written in class on **Wed Sep 9, 2026**
> and posted that evening. **All FILL fields were completed on 2026-09-10**, the day the
> scans were made and transcribed; the collection ran 2026-09-09.

## Source
Collected live by the GEOL 333/714 class at five pendulum stations in the D237 lab, Queens
College CUNY, Wed Sep 9, 2026, following the Pendulum Data Collection Sheet.

**Transcription flow, ruled 2026-09-07.** The paper sheets are the primary record. They are
collected at the end of the session and **inspected that evening for legibility**, while the
students who wrote them are still reachable and the session is fresh; anything unreadable is
resolved then, not in October. The sheets are then set aside and **formally scanned on the
morning of Thu Sep 10**, and the numbers are transcribed from those scans.

This replaces the earlier plan, in which readings were called out and typed during the class
break. That plan assumed one apparatus; five stations running in parallel produce five sheets
and 125 rows, which is more than a break absorbs, and typing under time pressure immediately
after teaching is where a digit goes wrong.

**Transcription is checked, not trusted.** `scripts/check_pendulum_inclass.py` runs three
layers against this file: structure (125 rows, stations A to E, five lengths, trials 1 to 5,
nothing missing or duplicated), arithmetic (`period_s` equals `t10_s / 10`, the one internal
redundancy the sheet provides), and physics (each period against `T = 2*pi*sqrt(l/g)`, reported
as a row to re-read rather than as an error, since real scatter is expected). The third layer
exists because the first two cannot see a value that is internally consistent but was read off
the wrong line of the sheet.

**Collected Wed 9 Sep 2026. Scanned and redacted 10 Sep 2026; transcribed from those scans the
same day.** All five stations ran and all five returned complete sheets.

Station anomalies, all recorded rather than corrected:

- **Three stations recopied their sheet.** B, C and E each rewrote page 1 after crossing out,
  so the scan holds eight page-1s for five stations. The clean copy was transcribed in each case.
- **Two stations averaged wrongly.** Station A wrote `1.53` in the period column for mark 2 trial 4
  where its own `t10` of 15.53 gives 1.553, then averaged the typo to 1.555; the five trials give
  1.5596. Station D wrote 1.5668 for mark 2; its five trials give 1.5608. Both were re-rendered at
  260 dpi and the digits confirmed, so these are the stations' arithmetic and not transcription.
  **Both wrong means went onto the E227 board**, so anything copied from the board carries them.
- **One mistimed trial survives in the data.** Station E, mark 2, trial 1 reads 13.76 s where theory
  gives about 15.77. Confirmed on the scan at 260 dpi, including the station's own derived 1.376.
  It is left in: the station recorded it and averaged it, and the checker flags it as a suspect.
- **Stations A and D wrote measured lengths in the sheet margin**, which the protocol did not ask for.

Each student also measured their own string's marks on a personal sheet. Those readings are kept
separately and are not part of this file, whose `length_m` is the nominal true length for every
station alike.

## License
Instructor- and class-created course data (GEOL 333/714, Fall 2026). No external license or
attribution constraint; free to post and redistribute as course content. Contains no student
names or identifiers: `station` is an apparatus label, never a person or group of people.

## Protocol
Five stations, each running the full protocol at its own apparatus: five true lengths
(0.4157, 0.6177, 0.8107, 1.0187, 1.2067 m), five trials per length, each trial timing ten complete
swings and dividing by ten, amplitude under 15°. **Length convention (ruled 2026-09-04):**
`length_m` is the true pendulum length, pivot to the center of the bob; strings are marked at
`l − 1.27 cm` so the mark sits at the top of the one-inch bob. 125 rows expected.

**125 rows delivered, none missing or duplicated.**

**One deviation from an earlier draft of this document**, which listed the true lengths as the round
0.400 to 1.200 m. The ruling of 2026-09-08 moved the mark targets to 40.3, 60.5, 79.8, 100.6 and
119.4 cm from the top of the bob, near-round so the five lengths stay spread while the decimal
cannot be guessed off the marking slip. True length is the target plus the 1.27 cm bob radius, so
the set is 0.4157, 0.6177, 0.8107, 1.0187 and 1.2067 m. `check_pendulum_inclass.py` still held the
round set and failed all 125 rows until it was corrected on 2026-09-10.

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
if per-trial scatter matches the sample's.

**Actual, from `np.polyfit(length_m, period_s ** 2, 1, cov=True)` over all 125 rows:**

| | |
|---|---|
| slope | 4.085 ± 0.045 s²/m |
| intercept | −0.159 ± 0.038 s² |
| **g** | **9.67 ± 0.11 m/s²** |
| distance to 9.81 | 1.4 σ |

σ_g came out near 0.11 rather than the 0.04 anticipated above, because the per-trial scatter is
roughly three times the sample CSV's: the per-length standard deviations run 0.027 to 0.049 s.

The intercept is not zero and it is worth a question rather than a shrug. Dividing it by the slope
turns it into a length offset of **−39 mm**, meaning the effective lengths were about four
centimetres shorter than the values in this file. The nine student sheets measured the marks about
1.3 cm short of their targets, which accounts for part of it and not all of it.

## Reproducibility
Primary record: the paper collection sheets (each carries its station letter) and the scans
made from them on Thu Sep 10, with this CSV as the transcription of those scans. Keep the
sheets; the scan is the readable copy, the paper is the original.

The file posts to three places once it passes `check_pendulum_inclass.py`: `outputs/data/`
(this repo), the public course-data mirror
`soule-geophysics/geol-333-714/data/pendulum_inclass.csv`, and the Brightspace Wk 2 page.
**HW0 depends on it by Sep 16**, so Thursday's scan-and-transcribe leaves five days of slack.
**Checker output, `scripts/check_pendulum_inclass.py`, 2026-09-10:**

```
expected shape: 5 stations x 5 lengths x 5 trials = 125 rows
structure  : PASS
arithmetic : PASS
physics    : 1 suspect row(s)
  LOOK  line 107: station E l=0.6177 trial 1: period 1.3760 s is 13% from theory 1.5766 s
```

**A fourth check, outside the script.** Each station wrote its own mean period per mark on page 2.
Those means were transcribed separately, off a different page, and every one of the twenty-five
columns was checked against them; twenty-three agree and the two that do not are the station
arithmetic errors above. Page 2 carries no station letter, so the mark-5 tails were joined by
inference: of the 120 possible assignments of tails to stations, **exactly one** reproduces every
station's own handwritten mark-5 mean, three of them exactly to four decimals.

Build commit `bd0252e`, trial-numbering fix `f0fad4d`.
