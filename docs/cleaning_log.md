# Cleaning log

All cleaning is done in **Power Query**, so every step is recorded and can be repeated with a refresh. The `Raw` query is left untouched. A second query, `Clean`, references `Raw` and applies the steps below. It is loaded to the `Clean` sheet.

## Steps applied

| # | Step | Columns | Why |
| --- | --- | --- | --- |
| 1 | Removed columns | `img`, `last_update` | Image paths and update dates are not used in the analysis |
| 2 | Trimmed text | `title`, `console`, `genre`, `publisher`, `developer` | Removes leading and trailing spaces so the same value always groups together |
| 3 | Cleaned text | Same 5 columns | Removes hidden non-printing characters |
| 4 | Replaced empty values with "Unknown" | `developer` | 17 developers were empty text. The dataset already uses "Unknown" as its placeholder (4,435 rows) |
| 5 | Added `release_year` | from `release_date` | Needed for trends by year and decade. Games with no date keep a blank year |
| 6 | Added `has_sales_data` (Yes/No) | from `total_sales` | Makes it easy to filter to the 18,922 games that have sales figures |

## Decisions

- **Blank sales stay blank, never 0.** A blank means VGChartz did not track that game. Replacing it with 0 would say the game sold nothing and would pull every average down.
- **Blank critic scores stay blank** for the same reason.
- **"Unknown" publishers and developers are kept.** These games still have sales, and pivots will show them as their own group.
- **No rows were removed.** Rows without sales are still useful for counting releases by year, genre and platform.

## Checks after cleaning

| Check | Result |
| --- | ---: |
| Clean rows | 64,016 (same as raw) |
| Empty developers | 0 |
| Rows with sales data | 18,922 |
| Rows with no release year | 7,051 |

The repeated title and console pairs (238) are reviewed on Day 3.
