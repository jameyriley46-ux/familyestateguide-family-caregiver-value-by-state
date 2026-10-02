# Family Caregiver Value by State: Home Health and Personal Care Aide Wages (BLS-only release)

State-by-state hourly and annual pay for home health and personal care aides (SOC 31-1120), BLS OEWS May 2025: the wage benchmark Family Estate Guide uses to value unpaid family caregiving.

**Live page:** https://familyestateguide.com/estate-planning-data/family-caregiver-value-by-state/  
**Publisher:** Family Estate Guide (https://familyestateguide.com)  
**Version:** 1.0.0 (2026-10-02)  
**License:** CC BY 4.0 (data). See LICENSE.

> Not legal, tax, financial or medical advice. Figures are estimates with sampling error; legal rules change. Verify anything important with the original source or a qualified professional.

## Files

| File | Rows | Contents |
|---|---|---|
| `data/aide_wages_by_state_may2025.csv` | 52 | 51 rows (50 states + DC) plus a United States row. |

Blank cells mean not available, not published or not applicable; they are never zero.

## Data dictionary

### `data/aide_wages_by_state_may2025.csv`

| Column | Description |
|---|---|
| `state` | State name (50 states + District of Columbia; some files add a United States row). |
| `aide_median_hourly` | Median hourly wage, home health and personal care aides (SOC 31-1120), USD, May 2025 (OEWS H_MEDIAN). |
| `aide_median_annual` | Median annual wage, USD (OEWS A_MEDIAN). |
| `aide_mean_hourly` | Mean hourly wage, USD (OEWS H_MEAN). |
| `aide_p10_hourly` | 10th-percentile hourly wage, USD (OEWS H_PCT10). |
| `aide_p25_hourly` | 25th-percentile hourly wage, USD (OEWS H_PCT25). |
| `aide_p75_hourly` | 75th-percentile hourly wage, USD (OEWS H_PCT75). |
| `aide_p90_hourly` | 90th-percentile hourly wage, USD (OEWS H_PCT90). |
| `oews_aide_employment` | Number of wage-and-salary jobs in SOC 31-1120 (OEWS TOT_EMP). |
| `aide_median_vs_us_pct` | Percent difference between the state median hourly wage and the U.S. median ($17.21). Calculated by FEG. |
| `rank_aide_median_hourly` | Rank of the state median hourly wage, 1 = highest (51 jurisdictions; ties share the lower rank number). Blank for the U.S. row. |

## Sources

- U.S. Bureau of Labor Statistics, Occupational Employment and Wage Statistics (OEWS), May 2025 estimates (state file oesm25st.zip, national file oesm25nat.zip). https://www.bls.gov/oes/tables.htm . Public domain (U.S. government work).

## Methodology

- Rows for SOC 31-1120 (home health and personal care aides) were taken from the OEWS May 2025 state file (AREA_TYPE 2; Guam, Puerto Rico and the Virgin Islands dropped) and the national file (O_GROUP = detailed).
- The live page multiplies these wages by AARP's state estimates of family-caregiving hours. Those AARP figures and every column derived from them are NOT in this release (see Rights exclusions). Users who have their own hours estimate can multiply it by `aide_median_hourly`.

## Limitations

- OEWS publishes only the combined 31-1120 code; home health aides (31-1121) and personal care aides (31-1122) are not separated at the state level.
- OEWS excludes self-employed workers and workers employed directly by private households, so wages reflect agency, facility and organization jobs.
- Wages are what aides earn, not what agencies charge families (agency prices are higher).
- OEWS estimates have sampling error; neighbouring ranks may not be statistically different.

## Rights review and exclusions

Family Estate Guide publishes here only its own compiled data and U.S. government public-domain data (Census, BLS, CMS, DOL), plus third-party data that is under CC BY or a compatible open license, with attribution. Third-party copyrighted or non-commercial-licensed data is excluded.

- Removed all AARP Public Policy Institute 'Valuing the Invaluable 2026' data (Table A1): `aarp_smaller_state_flag`, `aarp_caregivers`, `aarp_care_hours_millions`, `aarp_value_millions`, `aarp_value_per_hour`. AARP's report is copyrighted and not released under an open license.
- Removed columns computed from AARP figures: `care_hours_per_caregiver_year`, `care_hours_per_caregiver_week`, `value_per_caregiver_at_aide_median`, `total_value_at_aide_median_millions`, `aarp_rate_minus_aide_median`, `rank_value_per_caregiver`, `rank_total_value`.
- Result: the headline 'value of family caregiving' figures on the live page are not reproduced here; only the public-domain BLS wage inputs are.

## How to cite

Family Estate Guide (2026). *Family Caregiver Value by State: Home Health and Personal Care Aide Wages (BLS-only release)* (Version 1.0.0) [Data set]. https://familyestateguide.com/estate-planning-data/family-caregiver-value-by-state/ . GitHub: https://github.com/jameyriley46-ux/familyestateguide-family-caregiver-value-by-state

A Zenodo DOI will be added here once version 1.0.0 is released and archived. Machine-readable citation: `CITATION.cff`.

Please link to the live page when you use the data.

## License

Data in this repository is licensed under the Creative Commons Attribution 4.0 International license (CC BY 4.0). Underlying U.S. government data is public domain; third-party CC BY data keeps its original attribution requirements (see Sources).
