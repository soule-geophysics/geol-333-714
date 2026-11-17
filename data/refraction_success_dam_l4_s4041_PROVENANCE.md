# `refraction_success_dam_l4_s4041.csv`: Provenance

## Source

**Real field data.** First-break picks from a shallow seismic refraction survey in the Success Dam spillway, Porterville, California, by the U.S. Geological Survey with the U.S. Army Corps of Engineers, Sacramento District. The picks were made by the U.S. Geological Survey and are used unchanged.

> Burton, B.L., Hunter, L.E., Cox, E.M., Lindsay, K.M., Galloway, R.G., and Nguyen, H., 2020, Success Dam Spillway seismic refraction survey, Porterville, California, December 2018 and July 2019: U.S. Geological Survey data release, https://doi.org/10.5066/P96U1EYD.

- Release: https://doi.org/10.5066/P96U1EYD (ScienceBase item 5d7684fde4b0c4f70d01fc1f)
- Child item: "Velocity models and first break picks, Success Dam spillway seismic refraction survey, Porterville, California" (ScienceBase item 5d76996ee4b0c4f70d01fdf0)
- File: `SuccessSeismic_FirstBreakTT.csv` (10,362,728 bytes), with `SuccessSeismic_DataDictionary_FirstBreakTT.csv`
- Retrieved: 2026-11-07, one GET each, from the ScienceBase file links of the child item
- SHA-256 of the pick file as retrieved: `830703feac6b5d5c6ae8e484cd2f3a2bc35a2155e060319e86423b679ee10bc3`
- SHA-256 of the data dictionary: `9c25bb51be4b575a6b290a049097ff0fd8da5a1b06786ea0e3fa1bc1325610b7`

Record used: Line 4, shot file 4041 (`ShotNum` 41), shot at station 73.5. Line 4 has 96 geophones at 6 ft (1.83 m), 40 Hz. The shot notes list file 4041 as "AWD", the release's 100-lb truck-mounted accelerated weight drop.

## License

Public domain (U.S. Government work). U.S. Geological Survey data are works of the U.S. Government and are in the public domain in the United States.

The FGDC metadata (`SuccessSeismic_2018_2019_IntVelModels.xml`, retrieved 2026-11-07) states these use constraints, quoted in part:

> "Any user who modifies the data is obligated to describe the types of modifications they perform. ... Acknowledgment of the U.S. Geological Survey would be appreciated in products derived from these data. User specifically agrees not to misrepresent the data, nor to imply that changes made were approved or endorsed by the U.S. Geological Survey."

The modifications are described under the extraction steps below.

## Columns

| Column | Unit | Meaning |
|---|---|---|
| `offset_m` | m | Distance from the shot station to the geophone station along the line |
| `first_break_ms` | ms | First-break pick time, `FBP_ms` in the source, unchanged |
| `travel_time_s` | s | `first_break_ms` / 1000 |

33 rows, offsets 0.91 m to 59.44 m at 1.83 m spacing, no missing picks. Picks are quantized to the 0.25 ms sample interval.

## Reproducibility: extraction

Script: `scripts/extract_success_dam_refraction.py`. Test: `tests/test_extract_success_dam_refraction.py`.

1. From the full pick file keep the rows with `Line == 4` and `ShotNum == 41`, every column unchanged. These 97 rows (96 geophones plus the shot row) are committed as `outputs/data/raw/success_dam_firstbreak_tt_l4_s41.csv`. The full 10 MB file is gitignored.
2. Keep geophone rows (`Trace > 0`) on the northwest side of the shot (`Trace_stn < ShotPos_Stn`, with `ShotPos_Stn` = 73.5). Drop rows with `FBP_ms == -1` (no pick); none fall inside 60 m.
3. Offset in meters = (73.5 minus `Trace_stn`) x 6 ft x 0.3048 m/ft, rounded to 0.001 m. The data dictionary gives 6 ft station spacing for lines 1 to 13.
4. Keep offsets up to 60 m.
5. `travel_time_s` = `first_break_ms` / 1000.

No pick was edited or removed for fit quality. The source column `ShotOffsetCorr_ms` and the tomographic model columns are not used.

Surface elevation (`NAVD88`, ft) over the 33 geophones runs from 652.2 to 653.0 ft, a range of 0.25 m. The spread is treated as flat.

## Reproducibility: rerun

```
uv run python scripts/extract_success_dam_refraction.py
```

The script reads the full pick file if it is present and otherwise the committed subset, writes the CSV, and prints the HW5b fit.
