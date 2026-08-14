# `profile.csv`: Provenance

## Source
Parsekian, A. (n.d.). *IGUaNA Unit 3: Gravity and Magnetics Field Data Exercises, Part 1 (USF GeoPark sinkhole gravity transect).* Science Education Resource Center, Carleton College.
URL: <https://serc.carleton.edu/iguana/teaching_materials/grav_mag/unit3.html>
Original file: `iguana_gravity_lab.v5.xlsx` (preserved at `outputs/data/raw/iguana_part1_geopark_sinkhole.xlsx`).

## Survey context
Linear gravity transect across a known karst sinkhole at the University of South Florida GeoPark, Tampa, FL. Survey ran in **three field sessions**:

| Date | Local time | Profile coverage (along-profile m) |
|---|---|---|
| 2019-04-04 | 18:29 – 19:25 EST | 110, 120, 130, 140, 150 (south of base) |
| 2019-04-06 | 10:27 – 12:24 EST | 50, 60, 70, 80, 90, 160, 170, 180, 190, 200 (50–90 north of base, 160–200 south) |
| 2019-04-18 | 15:52 – 17:12 EST | 0, 10, 20, 30, 40 (north of base) |

**Profile direction (verified against the CSV 2026-06-15):** the along-profile coordinate increases toward the **south**. UTM northing decreases monotonically as the coordinate rises (along=0 m is the northernmost point at northing 3104789, along=200 m is the southernmost at 3104620). So relative to the base at 100 m, points 0–90 are north of base and points 110–200 are south. (An earlier version of this table under-counted the Apr 6 stations and inverted the north/south labels; corrected here to match `profile.csv`.)

Base station at along-profile coordinate 100 m was re-occupied between every science station so a per-day linear drift can be fit and subtracted. The day-3 mean base reading sits ~0.11 mGal lower than days 1–2. This is long-term instrument drift across the 12-day gap (or a re-zero between sessions), and it's why each day must be tied to its own base mean before days are combined into a single profile.

## License
CC-BY-NC-SA 4.0 (per SERC reuse model). Attribution to A. Parsekian, University of Wyoming, IGUaNA / SERC.

## Citation block (paste into HW2 notebook header, `HW2_profile.ipynb`)
> Profile gravity dataset: Parsekian, A. (n.d.). IGUaNA Unit 3: Gravity and Magnetics Field Data Exercises, Part 1 (USF GeoPark sinkhole survey). Science Education Resource Center, Carleton College. CC-BY-NC-SA 4.0. https://serc.carleton.edu/iguana/teaching_materials/grav_mag/unit3.html

## Columns
| name | unit | description |
|---|---|---|
| `tag` | label | station name; `base100*` denotes a base re-occupation (suffix increments per visit) |
| `northing_m` | m | UTM Zone 17N northing |
| `easting_m` | m | UTM Zone 17N easting |
| `lat_deg` | deg | latitude (WGS-84) |
| `lon_deg` | deg | longitude (WGS-84) |
| `elev_rel_base_m` | m | elevation relative to base-station elevation |
| `point_along_profile_m` | m | along-profile coordinate; base station is at 100 m |
| `time_est` | datetime | local clock time of reading |
| `time_since_beg_min` | min | minutes since first reading (negative for before, positive for after) |
| `gravity_mgal` | mGal | absolute gravimeter reading |
| `sd_mgal` | mGal | instrument uncertainty (1σ) |
| `is_base` | bool | True if this row is a base re-occupation |

## Structure notes
- 43 rows total: 23 base re-occupations + 20 science stations.
- Profile spans points 0 → 200 m, with the base at 100 m.
- Three-day acquisition (see survey context table above). Drift fits should be done **per day**, not across the gaps.
- Days are tied together by referencing each science reading to its own day's mean base value (after per-day drift correction). This puts all three days on a common relative-gravity baseline.
- Sinkhole target produces a residual Bouguer anomaly visible after per-day drift correction, base-tie, free-air correction, and Bouguer correction.

## Cleanup applied
- Read `raw_data` sheet with header at row index 2 (rows 0–1 are page metadata).
- Renamed columns to snake_case (`Lattitude` typo silently corrected → `lat_deg`).
- Dropped trailing all-NaN rows.
- Added derived `is_base` column for quick filtering.
- Rounded UTM coords to 3 dp, lat/lon to 6 dp, gravity/SD to 6 dp.

## Reproducibility
`scripts/convert_iguana_xlsx_to_csv.py` regenerates this CSV from the .xlsx in `outputs/data/raw/`. Run with `uv run scripts/convert_iguana_xlsx_to_csv.py`.
