# Analysis notes

Findings from the PivotTables in `excel/video_game_sales_analysis.xlsx`. Sales are in millions of units.

## 1. Sales trend by decade and year (`Trend` sheet)

**PivotTable 1: Sales and releases by decade** (all 63,995 games)

| Decade | Total Sales (M units) | Games Released |
| --- | ---: | ---: |
| 1970s | 5.17 | 67 |
| 1980s | 102.49 | 1,947 |
| 1990s | 643.58 | 10,351 |
| 2000s | 3,324.95 | 21,801 |
| 2010s | 2,518.93 | 20,606 |
| 2020s | 3.45 | 2,172 |
| Unknown | 6.59 | 7,051 |
| **Total** | **6,605.16** | **63,995** |

**PivotTable 2: Sales by release year**, filtered to `data_period = Tracked (up to 2018)`. Total: 6,592.57M units.

**Findings**

- **The 2000s were the biggest decade,** with 3,324.95M units sold, about half of all tracked sales.
- **Sales peaked in 2008 at 538.09M units,** during the Wii, Xbox 360, PS3 and DS generation. 2007 to 2011 were the five strongest years.
- **Sales fell steadily after 2011,** down to 148.03M in 2018. Part of this drop is real (the shift to digital and mobile) and part comes from VGChartz tracking fewer games over time.
- **The 2020s show only 3.45M units** even though 2,172 games were released. This reflects missing data, not a market collapse, which is why years after 2018 are filtered out of the trend.
