# Data dictionary

**File:** `data/raw/vgchartz-2024.csv`
**Source:** [Video Game Sales 2024](https://www.kaggle.com/datasets/asaniczka/video-game-sales-2024) on Kaggle, collected from VGChartz
**Size:** 64,016 rows × 14 columns. Each row is one game on one platform.

| Column | Type | Description | Missing values |
| --- | --- | --- | --- |
| `img` | Text | Path to the box art image on VGChartz | 0 |
| `title` | Text | Game title | 0 |
| `console` | Text | Platform the game was released on, e.g. PS4, Switch, PC (81 platforms) | 0 |
| `genre` | Text | Game genre, e.g. Action, Shooter, Sports (20 genres) | 0 |
| `publisher` | Text | Company that published the game (3,383 publishers) | 0 |
| `developer` | Text | Studio that developed the game | 17 |
| `critic_score` | Number | Average critic score out of 10 | 57,338 |
| `total_sales` | Number | Worldwide units sold, in millions | 45,094 |
| `na_sales` | Number | North America units sold, in millions | 51,379 |
| `jp_sales` | Number | Japan units sold, in millions | 57,290 |
| `pal_sales` | Number | Europe and other PAL-region units sold, in millions | 51,192 |
| `other_sales` | Number | Rest of world units sold, in millions | 48,888 |
| `release_date` | Date | Release date (YYYY-MM-DD), from 1971 to 2024 | 7,051 |
| `last_update` | Date | Date VGChartz last updated the record | 46,137 |

## Notes

- Sales figures are VGChartz estimates of physical and digital units, not revenue.
- Only 18,922 rows have `total_sales`. VGChartz stopped estimating most sales after 2018, so years from 2019 onwards have very few sales figures.
- 225 title and console pairs appear more than once and will be checked during cleaning.
