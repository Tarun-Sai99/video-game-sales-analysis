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
| 6 | Added `has_sales_data` (Yes/No) | from `total_sales` | Makes it easy to filter to the games that have sales figures |
| 7 | Removed exact duplicate rows | All columns | 21 rows were exact copies of another row in every column |
| 8 | Added `data_period` | from `release_year` | Labels each game "Tracked (up to 2018)", "Incomplete (2019+)" or "Unknown year", because VGChartz stopped tracking most sales after 2018 |

## Decisions

- **Blank sales stay blank, never 0.** A blank means VGChartz did not track that game. Replacing it with 0 would say the game sold nothing and would pull every average down.
- **Blank critic scores stay blank** for the same reason.
- **"Unknown" publishers and developers are kept.** These games still have sales, and pivots will show them as their own group.
- **Only exact duplicates were removed.** Rows without sales are still useful for counting releases by year, genre and platform.
- **Repeated title and console pairs that differ in any column are kept.** Of the 238 repeated pairs, most have a different release date, publisher or sales figure. They look like re-releases or regional versions, not copies.
- **Sales trends are only reliable up to 2018.** Only 63 games released from 2019 onwards have sales figures, so charts by year use `data_period` to keep those years separate.

## Checks after cleaning

| Check | Result |
| --- | ---: |
| Clean rows | 63,995 (64,016 raw minus 21 exact duplicates) |
| Empty developers | 0 |
| Rows with sales data | 18,919 |
| Rows with no release year | 7,051 |
| Tracked (up to 2018) | 53,482 |
| Incomplete (2019+) | 3,462 |
