# Video Game Sales Analysis (Excel)

An end-to-end data analysis of global video game sales using **Microsoft Excel**, covering data profiling, data cleaning, pivot tables, charts and an interactive dashboard.

## Business questions

1. How did the global video game market grow and decline over the years?
2. Which genres sell best, and how has the genre mix changed by decade?
3. Which platforms and console makers dominated each era?
4. Who are the top publishers, and what are the best-selling games?
5. How do buying patterns differ between North America, Europe/PAL and Japan?

## Dataset

[Video Game Sales 2024](https://www.kaggle.com/datasets/asaniczka/video-game-sales-2024) from Kaggle, collected from VGChartz. It covers about 64,000 game releases from 1971 to 2024, with sales in millions of units by region, critic scores and release dates.

## Tools

- Microsoft Excel 2021: Power Query, PivotTables, PivotCharts, slicers, XLOOKUP

## Repository structure

| Path | What it holds |
|---|---|
| `data/raw/vgchartz-2024.csv` | Original dataset, unchanged |
| `excel/video_game_sales_analysis.xlsx` | Excel workbook: Power Query cleaning, profiling and PivotTables |
| `docs/data_dictionary.md` | What each column means |
| `docs/data_profiling.md` | Row counts, missing values and data quality checks |
| `docs/cleaning_log.md` | Every cleaning step and the reason for it |
| `docs/analysis_notes.md` | Findings from each analysis |

## Project status

Work in progress.

- [x] Load the raw data and write the data dictionary
- [x] Profile the data (missing values, duplicates, incomplete years)
- [x] Clean the data in Power Query (21 duplicates removed, helper columns for decade, data period and platform family)
- [x] Sales trend by decade and year (Question 1)
- [x] Genre performance by decade (Question 2)
- [x] Platform dominance by era (Question 3)
- [ ] Top publishers and best-selling games (Question 4)
- [ ] Regional comparison (Question 5)
- [ ] Charts and interactive dashboard
- [ ] Key insights summary

## Early findings

- Sales tracked by VGChartz peaked in **2008 at 538 million units**. The 2000s were the biggest decade (3,325 million units).
- **Sports, Action and Shooter** games make up half of all tracked sales. Shooters were the top genre of the 2010s.
- **Sony** has led every decade since the 1990s and accounts for about half of all tracked sales. **Microsoft** grew from 17% of sales in the 2000s to 31% in the 2010s, passing Nintendo.
- VGChartz stopped tracking most sales after 2018, so trend analysis uses releases up to 2018 only. See the [cleaning log](docs/cleaning_log.md).
