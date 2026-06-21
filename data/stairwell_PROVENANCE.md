# `stairwell.csv`: Provenance

## Source
Parsekian, A. (n.d.). *IGUaNA Unit 3: Gravity and Magnetics Field Data Exercises, Part 3a (Stairwell gravity).* Science Education Resource Center, Carleton College.
URL: <https://serc.carleton.edu/iguana/teaching_materials/grav_mag/unit3.html>
Original file: `iguana_maggrav_unit3_part3a_data.v4.xlsx` (preserved at `outputs/data/raw/iguana_part3a_stairwell.xlsx`).

## License
CC-BY-NC-SA 4.0 (per SERC reuse model). Attribution to A. Parsekian, University of Wyoming, IGUaNA / SERC.

## Citation block (paste into HW1 notebook header, `HW1_stairwell.ipynb`)
> Stairwell gravity dataset: Parsekian, A. (n.d.). IGUaNA Unit 3: Gravity and Magnetics Field Data Exercises, Part 3a. Science Education Resource Center, Carleton College. CC-BY-NC-SA 4.0. https://serc.carleton.edu/iguana/teaching_materials/grav_mag/unit3.html

## Columns
| name | unit | description |
|---|---|---|
| `station` | label | floor identifier (`Ground level`, `0.5`, `1`, …, `4.5`, `gound level`) |
| `time` | HH:MM:SS | clock time of the reading |
| `minutes_since_start` | min | elapsed time since the first reading (derived from `time`); numeric time axis for the HW1 drift-vs-time fit |
| `elevation_m` | m | elevation above the ground-floor base reference |
| `reading_mgal` | mGal | absolute gravimeter reading |
| `relative_mgal` | mGal | reading − ground-floor reference |
| `uncertainty_mgal` | mGal | instrument uncertainty (1σ) |

## Structure notes
- 11 rows: 1 ground-level open + 9 stairwell stations (0.5 → 4.5) + 1 ground-level close.
- Open and close ground-level reads enable a two-point linear drift correction.
- Single read per station: does **not** support stacking; the stacking concept is carried by the pendulum trial-stacks (HW0) and the profile base re-occupations (HW2).

## Cleanup applied
- Selected the first 6 columns of the `grav_stairwell` sheet (the trailing columns are student fill-in scaffolding).
- Dropped helper rows below row 11 (all NaN).
- Rounded float columns to 6 decimal places to suppress Excel→pandas precision noise.
- Added a derived `minutes_since_start` column (minutes elapsed since the first reading, computed from the `time` column) so HW1 can fit drift against a numeric time axis rather than an HH:MM:SS string (eval finding 5).
- Preserved the original `gound level` typo on the closing read for fidelity to source.

## Reproducibility
`scripts/convert_iguana_xlsx_to_csv.py` regenerates this CSV from the .xlsx in `outputs/data/raw/`. Run with `uv run scripts/convert_iguana_xlsx_to_csv.py`.
