# Data Cleaning Decisions

This document summarizes the decisions made in `clean_datasets.ipynb`. The cleaning code was written by Saanvi; this summary was written by Inseo to document the decision-making process.

## Scope
- Airport: O'Hare (ORD) only
- Period: January 2026 only

## Flights (BTS On-Time data -> flights_ord_jan2026_clean.csv)
- Standardized `ORIGIN` (trimmed whitespace, uppercase) and parsed `FL_DATE` to a date.
- Kept only flights with `ORIGIN == "ORD"` and `FL_DATE` in January 2026.
- Checked for duplicate rows: 0 found. 25,131 rows saved.
- 909 rows have a missing `DEP_DELAY`. All 909 are canceled flights, and no non-canceled flight has a missing delay. These rows were kept with the delay left blank so they count toward the cancellation rate.

## Airports (OpenFlights -> airports_ord_clean.csv)
- The source file has no header, so column names were added and `\N` values were read as missing.
- Kept only the ORD record and the columns `iata`, `icao`, `name`, `latitude`, `longitude`, `timezone`. The notebook checks that exactly one record remains.

## Weather (NOAA LCD station USW00094846 -> weather_ord_jan2026_clean.csv)
- Parsed `DATE` and kept January 2026 only.
- Kept rows with at least one reading among temperature, precipitation, wind speed, and visibility.
- Kept columns: `STATION`, `DATE`, `REPORT_TYPE`, `SOURCE` and the four weather fields. Added an `iata` column set to `ORD` as the join key.
- Checked for duplicate rows: 0 found. 1,311 rows saved.
- Missing values: `HourlyPrecipitation` is blank in 883 rows. The other three weather fields have none.

## Open issues for the merge
- `CRS_DEP_TIME` is stored as HHMM (e.g., 700), so a datetime must be built from `FL_DATE` and `CRS_DEP_TIME`.
- The weather file mixes report types (e.g., FM-15 and FM-12), so there is more than one observation per hour. Merging needs to avoid duplicating flights.
- Blank `HourlyPrecipitation` values need a decision: no precipitation or not observed.
- Raw input files are not in the repository, so the notebook cannot be rerun as is.
