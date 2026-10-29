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

## 2. Genre performance by decade (`Genre` sheet)

PivotTable with genre as rows and decade as columns, filtered to `data_period = Tracked (up to 2018)` and sorted by total sales.

| Genre | 1980s | 1990s | 2000s | 2010s | Total |
| --- | ---: | ---: | ---: | ---: | ---: |
| Sports | 7.53 | 132.67 | 619.52 | 426.83 | 1,186.70 |
| Action | 27.91 | 68.56 | 573.81 | 451.37 | 1,124.39 |
| Shooter | 26.50 | 46.19 | 361.39 | 560.41 | 995.47 |
| Misc | 0.51 | 39.51 | 342.21 | 174.30 | 556.53 |
| Racing | 2.92 | 75.59 | 333.18 | 111.44 | 523.40 |
| Role-Playing | 4.36 | 34.15 | 170.03 | 213.83 | 422.37 |
| Platform | 21.78 | 45.20 | 210.14 | 71.99 | 349.11 |
| Fighting | 2.29 | 84.30 | 170.67 | 83.13 | 340.39 |

Top 8 of 20 genres shown. The 1970s (5.17M in total) are left out of this table.

**Findings**

- **Sports, Action and Shooter are the top 3 genres,** with 50% of all tracked sales between them (3,306.56M of 6,592.57M).
- **Shooters overtook every other genre in the 2010s** (560.41M), up from 4th place in the 2000s. Sports led the 2000s (619.52M).
- **Platform games peaked early.** They were the 3rd biggest genre of the 1980s (21.78M, behind Action and Shooter) but fell to 71.99M in the 2010s.
- **Fighting games had their best share in the 1990s** (84.30M, the 2nd biggest genre that decade, behind Sports).
- **Role-Playing grew from the 2000s to the 2010s** (170.03M to 213.83M) while most genres shrank. Shooter, Action-Adventure and Music also grew.
