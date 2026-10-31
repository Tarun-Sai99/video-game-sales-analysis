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

## 3. Platform dominance by era (`Platform` sheet)

Two PivotTables with `platform_family` as rows and decade as columns, both filtered to `data_period = Tracked (up to 2018)` and sorted by total sales.

**PivotTable 1: Total sales (M units)**

| Platform family | 1970s | 1980s | 1990s | 2000s | 2010s | Total |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| Sony | | | 394.22 | 1,645.48 | 1,219.29 | 3,258.99 |
| Nintendo | | 32.33 | 163.55 | 1,032.98 | 430.92 | 1,659.78 |
| Microsoft | | | | 578.12 | 782.50 | 1,360.62 |
| PC | | 0.03 | 24.42 | 60.26 | 83.67 | 168.38 |
| Atari | 5.17 | 70.13 | 0.15 | | | 75.45 |
| Sega | | | 58.96 | 7.11 | | 66.07 |
| Other | | | 2.28 | 0.97 | | 3.25 |
| Mobile | | | | 0.03 | | 0.03 |
| **Total** | **5.17** | **102.49** | **643.58** | **3,324.95** | **2,516.38** | **6,592.57** |

**PivotTable 2: Market share within each decade** (Show Values As: % of Column Total)

| Platform family | 1970s | 1980s | 1990s | 2000s | 2010s | Overall |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| Sony | 0.00% | 0.00% | 61.25% | 49.49% | 48.45% | 49.43% |
| Nintendo | 0.00% | 31.54% | 25.41% | 31.07% | 17.12% | 25.18% |
| Microsoft | 0.00% | 0.00% | 0.00% | 17.39% | 31.10% | 20.64% |
| PC | 0.00% | 0.03% | 3.79% | 1.81% | 3.33% | 2.55% |
| Atari | 100.00% | 68.43% | 0.02% | 0.00% | 0.00% | 1.14% |
| Sega | 0.00% | 0.00% | 9.16% | 0.21% | 0.00% | 1.00% |

**Findings**

- **Each era had a clear leader.** Atari owned the 1970s and 1980s (68% of 1980s sales), then Sony took over in the 1990s with 61% and led every decade after that.
- **Sony accounts for about half of all tracked sales** (3,258.99M units, 49%), almost twice as much as Nintendo.
- **Microsoft grew fast.** It went from 17% of sales in the 2000s to 31% in the 2010s and passed Nintendo, whose share fell from 31% to 17%.
- **Sega disappeared after the 1990s.** It had 9% of 1990s sales but only 0.21% in the 2000s, after it stopped making consoles.
- **PC and Mobile look small here,** but that is mostly a data gap: VGChartz tracks boxed retail sales and misses digital downloads and app stores, where most PC and mobile games are sold.

## 4. Top publishers and best-selling games (`Publishers` sheet)

Two PivotTables, both filtered to `data_period = Tracked (up to 2018)`, using a Top 10 value filter and sorted by total sales.

**PivotTable 1: Top 10 publishers**

| Publisher | Total Sales (M units) | Games with Sales |
| --- | ---: | ---: |
| Activision | 722.77 | 1,044 |
| Electronic Arts | 644.13 | 843 |
| EA Sports | 485.66 | 540 |
| Ubisoft | 462.28 | 1,011 |
| THQ | 320.89 | 726 |
| Sony Computer Entertainment | 310.82 | 567 |
| Rockstar Games | 239.67 | 93 |
| Konami | 210.70 | 769 |
| Sega | 206.14 | 639 |
| Nintendo | 139.91 | 381 |
| **Top 10 total** | **3,742.97** | **6,613** |

**PivotTable 2: Top 10 best-selling games** (sales added up across all platforms a game was released on)

| Game | Total Sales (M units) |
| --- | ---: |
| Grand Theft Auto V | 64.29 |
| Call of Duty: Black Ops | 30.99 |
| Call of Duty: Modern Warfare 3 | 30.71 |
| Call of Duty: Black Ops II | 29.59 |
| Call of Duty: Ghosts | 28.80 |
| Call of Duty: Black Ops 3 | 26.72 |
| Call of Duty: Modern Warfare 2 | 25.02 |
| Minecraft | 24.01 |
| Grand Theft Auto IV | 22.53 |
| Call of Duty: Advanced Warfare | 21.78 |
| **Top 10 total** | **304.44** |

**Findings**

- **The top 10 publishers sold 3,742.97M units,** 57% of all tracked sales (6,592.57M).
- **Activision is the biggest publisher** (722.77M), mostly thanks to Call of Duty, which holds 7 of the top 10 game spots.
- **Electronic Arts is even bigger if its sports label is counted.** The data lists "Electronic Arts" and "EA Sports" as separate publishers. Together they reach 1,129.79M, more than Activision. They are kept separate here to match the source data.
- **Rockstar Games sells far more per game than anyone else.** It reached 239.67M from only 93 games (about 2.6M per game), while Activision needed 1,044 games. Grand Theft Auto V alone sold 64.29M, more than twice the next game.
- **Nintendo looks too small, which is a data gap.** In the whole dataset, only 383 of the 1,474 games Nintendo published have sales figures, and big hits like Mario Kart Wii and Mario Kart 8 Deluxe have none. Nintendo's real sales are much higher than this dataset shows.

## 5. Regional comparison (`Regions` sheet)

Two PivotTables with genre as rows and one column per region, both filtered to `data_period = Tracked (up to 2018)` and sorted by North America sales. The second table uses Show Values As: % of Column Total, so each region adds up to 100% and shows that region's genre mix. A colour scale highlights the biggest shares.

**Regional totals (M units)**

| Region | Total Sales | Share of tracked sales |
| --- | ---: | ---: |
| North America | 3,344.24 | 51% |
| Europe (PAL) | 1,914.23 | 29% |
| Japan | 679.25 | 10% |
| Other Regions | 650.41 | 10% |

**Genre mix by region (% of each region's sales), top genres**

| Genre | North America | Europe (PAL) | Japan | Other Regions |
| --- | ---: | ---: | ---: | ---: |
| Sports | 18.16% | 17.84% | 16.04% | 19.70% |
| Action | 17.62% | 17.88% | 11.68% | 17.28% |
| Shooter | 15.80% | 16.96% | 5.00% | 16.67% |
| Misc | 8.84% | 7.65% | 8.16% | 8.99% |
| Racing | 8.07% | 9.28% | 2.90% | 8.62% |
| Role-Playing | 5.13% | 4.75% | 18.63% | 5.18% |
| Fighting | 5.20% | 4.17% | 8.56% | 4.39% |
| Strategy | 1.41% | 1.41% | 5.40% | 1.12% |

**Findings**

- **North America is half the market,** with 3,344.24M units (51% of tracked sales). Europe is second with 29%. Japan and all other regions have about 10% each.
- **North America and Europe buy almost the same mix of games.** Sports, Action and Shooter are the top 3 in both, each at 16 to 18%.
- **Japan is very different.** Role-Playing is its #1 genre (18.63% of sales) but only about 5% in every other region. Fighting (8.56%), Strategy (5.40%) and Puzzle (4.28%) are also much more popular in Japan.
- **Shooters and Racing games barely sell in Japan.** Shooters are 5.00% of Japan's sales against 16 to 17% in the West, and Racing is 2.90% against 8 to 9%.
- **For a publisher, this means one global plan does not fit Japan.** A Western shooter can rely on North America and Europe, while an RPG needs Japan as a core market.
