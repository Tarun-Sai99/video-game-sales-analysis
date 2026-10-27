# Data profiling

Before cleaning, I profiled the raw data to see how complete each column is. The raw CSV is loaded into Excel with Power Query (UTF-8 encoding, with types detected from the entire dataset and sales columns set to Decimal Number). The profile is on the `Profile` sheet of `excel/video_game_sales_analysis.xlsx`.

## Column profile

| Column | Non-blank | Blank | % Blank | Distinct values | Min | Max |
| --- | ---: | ---: | ---: | ---: | --- | --- |
| title | 64,016 | 0 | 0% | 39,596 | | |
| console | 64,016 | 0 | 0% | 81 | | |
| genre | 64,016 | 0 | 0% | 20 | | |
| publisher | 64,016 | 0 | 0% | 3,383 | | |
| developer | 63,999 | 17 | 0% | 8,854 | | |
| critic_score | 6,678 | 57,338 | 90% | 89 | 1 | 10 |
| total_sales | 18,922 | 45,094 | 70% | 482 | 0 | 20.32 |
| na_sales | 12,637 | 51,379 | 80% | 320 | 0 | 9.76 |
| jp_sales | 6,726 | 57,290 | 89% | 121 | 0 | 2.13 |
| pal_sales | 12,824 | 51,192 | 80% | 256 | 0 | 9.85 |
| other_sales | 15,128 | 48,888 | 76% | 133 | 0 | 3.12 |
| release_date | 56,965 | 7,051 | 11% | 7,922 | 1971-12-03 | 2024-12-31 |
| last_update | 17,879 | 46,137 | 72% | 1,545 | 2017-11-28 | 2024-01-28 |

## Data quality checks

| Check | Result |
| --- | ---: |
| Total rows | 64,016 |
| Rows with sales data | 18,922 |
| Publisher = "Unknown" | 8,842 |
| Developer = "Unknown" | 4,435 |
| Games with 0 total sales | 1,352 |
| Repeated title + console pairs | 238 |

## Findings

- **Sales are missing for 70% of games.** Only 18,922 of 64,016 rows have `total_sales`. Blank sales mean "not tracked", not "zero sold", so they must stay blank.
- **The 17 blank developers are empty text, not true blanks.** `COUNTA` counted them as filled, so non-blank is calculated as `ROWS(Raw) - COUNTBLANK`.
- **"Unknown" is used as a placeholder** for 8,842 publishers and 4,435 developers.
- **Critic scores are rare (10% of rows),** so they can support side analysis only.
- **11% of games have no release date,** which affects any analysis by year.
- **238 title and console pairs repeat.** These need checking in case they are duplicates or separate regional releases.
- **`img` and `last_update` are not needed for the analysis.**
