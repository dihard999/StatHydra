# 🐉 StatHydra | Sports API and Machine Learning for Match Prediction
**This application is a powerful API for sports analytics and intelligent sports prediction system that combines analytics, machine learning and deep statistical approach. StatHydra provides accurate match predictions based on a large array of data, current news and unique algorithms for evaluating the form of teams and players. This is a tool for those who value awareness and data in the world of betting and sports.  
The brand's mission is to turn sports analytics into your reliable tool for winning, making every prediction informed, accurate and transparent.  
StatHydra is not just a prediction, it is your personal sports analyst who does not miss a single detail. We combine the power of artificial intelligence and love for sports so that your decisions are always one step ahead.  
When you need more than one point of view, choose StatHydra!**
> [!NOTE]
> **Development is only available for NHL, development of other sports is in progress....**  
> **The data starts from 2005-06 season. Of course, if most people need years earlier, we will consider this possibility.**  
> **Any requests to make additional filters based on the data are also welcome.**
---
---
# NHL API
1. [Base URL](#base-url)
2. [Player](#player)  
   2.1 [Get player leaders by year and all stat](#league_leaders_{year})  
   2.2 [Get player leaders by year and specific stat](#league_leaders_{year}/stat_abbrev/{stat_abbrev})  
   2.3 [Get player leaders by year and specific stat and rank](#league_leaders_{year}/stat_abbrev/{stat_abbrev}/rank/{rank})  
   2.4 [Get player leaders by year and specific stat and player ID](#league_leaders_{year}/stat_abbrev/{stat_abbrev}/player_id/{player_id})  
   2.5 [Get player leaders by year and specific stat and team](#league_leaders_{year}/stat_abbrev/{stat_abbrev}/team_abbrev/{team_abbrev})  
   2.6 [Get player leaders by year and specific rank](#league_leaders_{year}/rank/{rank})  
   2.7 [Get player leaders by year and specific rank and player ID](#league_leaders_{year}/rank/{rank}/player_id/{player_id})  
   2.8 [Get player leaders by year and specific rank and team](#league_leaders_{year}/rank/{rank}/team_abbrev/{team_abbrev})  
   2.9 [Get player leaders by year and specific player ID](#league_leaders_{year}/player_id/{player_id})  
   2.10 [Get player leaders by year and specific team](#league_leaders_{year}/team_abbrev/{team_abbrev})  
   2.11 [Get player leaders by year and specific team and player ID](#league_leaders_{year}/team_abbrev/{team_abbrev}/player_id/{player_id})  
   2.12 [Get basic stats players regular season by year](#basic_stats_players_regular_season_{year})  
   2.13 [Get basic stats players regular season by year and specific rank](#basic_stats_players_regular_season_{year}/rank/{rank})  
   2.14 [Get basic stats players regular season by year and specific team](#basic_stats_players_regular_season_{year}/team_abbrev/{team_abbrev})  
   2.15 [Get basic stats players regular season by year and player ID](#basic_stats_players_regular_season_{year}/player_id/{player_id})  
   2.16 [Get basic stats players regular season by year and position](#basic_stats_players_regular_season_{year}/position/{position})  
   2.17 [Get basic stats players playoff by year](#basic_stats_players_playoff_{year})  
   2.18 [Get basic stats players playoff by year and specific rank](#basic_stats_players_playoff_{year}/rank/{rank})  
   2.19 [Get basic stats players playoff by year and specific team](#basic_stats_players_playoff_{year}/team_abbrev/{team_abbrev})  
   2.20 [Get basic stats players playoff by year and player ID](#basic_stats_players_playoff_{year}/player_id/{player_id})  
   2.21 [Get basic stats players playoff by year and position](#basic_stats_players_playoff_{year}/position/{position})  
   2.22 [Get miscellaneous stats players regular season by year](#miscellaneous_stats_players_regular_season_{year})  
   2.23 [Get miscellaneous stats players regular season by year and specific rank](#miscellaneous_stats_players_regular_season_{year}/rank/{rank})  
   2.24 [Get miscellaneous stats players regular season by year and specific team](#miscellaneous_stats_players_regular_season_{year}/team_abbrev/{team_abbrev})  
   2.25 [Get miscellaneous stats players regular season by year and player ID](#miscellaneous_stats_players_regular_season_{year}/player_id/{player_id})  
   2.26 [Get miscellaneous stats players regular season by year and position](#miscellaneous_stats_players_regular_season_{year}/position/{position})  
   2.27 [Get miscellaneous stats players playoff by year](#miscellaneous_stats_players_playoff_{year})  
   2.28 [Get miscellaneous stats players playoff by year and specific rank](#miscellaneous_stats_players_playoff_{year}/rank/{rank})  
   2.29 [Get miscellaneous stats players playoff by year and specific team](#miscellaneous_stats_players_playoff_{year}/team_abbrev/{team_abbrev})  
   2.30 [Get miscellaneous stats players playoff by year and player ID](#miscellaneous_stats_players_playoff_{year}/player_id/{player_id})  
   2.31 [Get miscellaneous stats players playoff by year and position](#miscellaneous_stats_players_playoff_{year}/position/{position})  
   2.32 [Get hat tricks by year](#hat_tricks_{year})  
   2.33 [Get hat tricks by year and specific team](#hat_tricks_{year}/team_abbrev/{team_abbrev})  
   2.34 [Get hat tricks by year and player ID](#hat_tricks_{year}/player_id/{player_id})  
   2.35 [Get hat tricks by year and specific game](#hat_tricks_{year}/game_id/{game_id})  
   2.36 [Get hat tricks by year and specific date](#hat_tricks_{year}/game_date/{game_date})  
   2.37 [Get penalty shots by year](#penalty_shots_{year})  
   2.38 [Get penalty shots by year and specific team](#penalty_shots_{year}/team_abbrev/{team_abbrev})  
   2.39 [Get penalty shots by year and player ID](#penalty_shots_{year}/player_id/{player_id})  
   2.40 [Get penalty shots by year and specific game](#penalty_shots_{year}/game_id/{game_id})  
   2.41 [Get penalty shots by year and specific date](#penalty_shots_{year}/game_date/{game_date})  
   2.42 [Get advanced stats players by year](#advanced_stats_players_{year})  
   2.43 [Get advanced stats players by year and specific rank](#advanced_stats_players_{year}/rank/{rank})  
   2.44 [Get advanced stats players by year and player ID](#advanced_stats_players_{year}/player_id/{player_id})  
   2.45 [Get advanced stats players by year and specific team](#advanced_stats_players_{year}/team_abbrev/{team_abbrev})  
   2.46 [Get advanced stats players by year and position](#advanced_stats_players_{year}/position/{position})  
   2.47 [Get skater time on ice stats by year](#skater_time_on_ice_stats_{year})  
   2.48 [Get skater time on ice stats by year and specific rank](#skater_time_on_ice_stats_{year}/rank/{rank})  
   2.49 [Get skater time on ice stats by year and player ID](#skater_time_on_ice_stats_{year}/player_id/{player_id})  
   2.50 [Get skater time on ice stats by year and specific team](#skater_time_on_ice_stats_{year}/team_abbrev/{team_abbrev})  
   2.51 [Get skater time on ice stats by year and position](#skater_time_on_ice_stats_{year}/position/{position})  
3. [Team](#team)  
   3.1 [Get all season teams statistics summary(except for the current season)](#team_all_season_summary)  
   3.2 [Get all season teams statistics summary by specific team(except for the current season)](#team_all_season_summary/team_abbrev/{team_abbrev})  
   3.3 [Get teams analytics 5 on 5 by year](#team_analytics_5_on_5_{year})  
   3.4 [Get teams analytics 5 on 5 by year and specific team](#team_analytics_5_on_5_{year}/team_abbrev/{team_abbrev})  
   3.5 [Get expanded standings teams by year](#expanded_standings_{year})  
   3.6 [Get expanded standings teams by year and specific team](#expanded_standings_{year}/team_abbrev/{team_abbrev})  
   3.7 [Get expanded standings teams by year and specific rank](#expanded_standings_{year}/rank/{rank})  
   3.8 [Get team versus team by year](#team_vs_team_{year})  
   3.9 [Get team versus team by year and specific team](#team_vs_team_{year}/{team_abbrev})  
   3.10 [Get roster team by year](#roster_team_{year})  
   3.11 [Get roster team by year and specific team](#roster_team_{year}/team_abbrev/{team_abbrev})  
   3.12 [Get roster team by year and player ID](#roster_team_{year}/player_id/{player_id})  
   3.13 [Get roster team by year and position](#roster_team_{year}/position/{position})  
   3.14 [Get injuries team now](#injuries_now)  
   3.15 [Get injuries team now by specific team](#injuries_now/team_abbrev/{team_abbrev})  
   3.16 [Get injuries team now by player ID](#injuries_now/player_id/{player_id})  
   3.17 [Get scoring (period) by year](#scoring_by_period_{year})  
   3.18 [Get scoring (period) by year and specific team](#scoring_by_period_{year}/team_abbrev/{team_abbrev})  
   3.19 [Get shots (period) by year](#shots_by_period_{year})  
   3.20 [Get shots (period) by year and specific team](#shots_by_period_{year}/team_abbrev/{team_abbrev})  
   3.21 [Get miscellaneous records teams by year](#records_team_{year})  
   3.22 [Get miscellaneous records teams by year and specific team](#records_team_{year}/team_abbrev/{team_abbrev})  
5. [Season](#season)  
   4.1 [Get summary statistic season by year](#season_summary_{year})  
   4.2 [Get summary statistic season by year and specific team](#season_summary_{year}/team_abbrev/{team_abbrev})  
   4.3 [Get detail statistic season by year](#season_statistics_{year})  
   4.4 [Get detail statistic season by year and specific team](#season_statistics_{year}/team_abbrev/{team_abbrev})  
   4.5 [Get detail statistic season by year and specific rank](#season_statistics_{year}/rank/{rank})  
   4.6 [Get detail statistic season by year and playoff](#season_statistics_{year}/playoff/{playoff})  
   4.7 [Get league average by year](#league_average_{year})  
   4.8 [Get regular season schedule by year](#regular_season_schedule_{year})  
   4.9 [Get regular season schedule by year and specific date](#regular_season_schedule_{year}/game_date/{game_date})  
   4.10 [Get regular season schedule by year and specific game](#regular_season_schedule_{year}/game_id/{game_id})  
   4.11 [Get regular season schedule by year and specific team](#regular_season_schedule_{year}/team_abbrev/{team_abbrev})  
   4.12 [Get regular season schedule by year and finished game](#regular_season_schedule_{year}/finished)  
   4.13 [Get regular season schedule by year and upcoming game](#regular_season_schedule_{year}/upcoming)  
   4.14 [Get regular season schedule by year and upcoming game for next day](#regular_season_schedule_{year}/upcoming_day)  
   4.15 [Get regular season schedule by year and upcoming game for next week](#regular_season_schedule_{year}/upcoming_week)  
   4.16 [Get regular season schedule by year and upcoming game for next month](#regular_season_schedule_{year}/upcoming_month)  
6. [Playoff](#playoff)  
   5.1 [Get playoff result by year](#league_playoff_series_result_{year})  
   5.2 [Get playoff result by year and specific game](#league_playoff_series_result_{year}/game_id/{game_id})  
   5.3 [Get playoff result by year and specific date](#league_playoff_series_result_{year}/game_date/{game_date})  
   5.4 [Get playoff schedule by year](#playoff_schedule_{year})  
   5.5 [Get playoff schedule by year and specific date](#playoff_schedule_{year}/game_date/{game_date})  
   5.6 [Get playoff schedule by year and specific game](#playoff_schedule_{year}/game_id/{game_id})  
   5.7 [Get playoff schedule by year and specific team](#playoff_schedule_{year}/team_abbrev/{team_abbrev})  
   5.8 [Get playoff schedule by year and finished game](#playoff_schedule_{year}/finished)  
   5.9 [Get playoff schedule by year and upcoming game](#playoff_schedule_{year}/upcoming)  
   5.10 [Get playoff schedule by year and upcoming game for next day](#playoff_schedule_{year}/upcoming_day)  
   5.11 [Get playoff schedule by year and upcoming game for next week](#playoff_schedule_{year}/upcoming_week)  
   5.12 [Get playoff schedule by year and upcoming game for next month](#playoff_schedule_{year}/upcoming_month)  
---
<a name="base-url"></a>
## 1. Base URL
All endpoints referenced in this section are relative to the following base URL:  
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/
```
Your unique API Key required for accessing the API endpoints. Substitute YOUR_API_KEY with your actual key in the URL path.

---
<a name="player"></a>
## 2. Player
<a name="league_leaders_{year}"></a>
### 2.1 Get player leaders by year and all stat
- **Endpoint:** `/league_leaders_{year}/`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and all category.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`stat_name`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL"). Sometimes you can see the values ​​2TM, 3TM, etc. 2TM means the player played for 2 teams, 3TM - for three teams, etc.
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`stat_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:
    
| Stat name                                   | Short code |  
|---------------------------------------------|------------|  
| Assists                                    | A          |  
| Assists Per Game                           | APG        |  
| Defensive Point Shares                     | DPS        |  
| Even Strength Goals                        | EVSG       |  
| Expected +/-                               | XPM        |  
| Game-Winning Goals                         | GWG        |  
| Games Played (Goalie)                      | GPG        |  
| Goalie Point Shares                        | GPS        |  
| Goals                                      | G          |  
| Goals Against                              | GA         |  
| Goals Against Average                      | GAA        |  
| Goals Allowed Adjusted                     | GAAJ       |  
| Goals Created                              | GCR        |  
| Goals Created Per Game                     | GCPG       |  
| Goals Per Game                             | GPGM       |  
| Goals Saved Above Average                  | GSAA       |  
| Hat Tricks                                 | HTR        |  
| Losses                                     | L          |  
| Minutes                                    | MIN        |  
| Offensive Point Shares                     | OPS        |  
| Penalties in Minutes                       | PIM        |  
| Plus/Minus                                 | PLM        |  
| Point Shares                               | PTS        |  
| Points                                     | P          |  
| Points Per Game                            | PPG        |  
| Power Play Goals                           | PPGL       |  
| Power Play Goals On-Ice Against            | PGAI       |  
| Power Play Goals On-Ice For                | PGFI       |  
| Save Percentage                            | SVP        |  
| Saves                                      | SAV        |  
| Shooting Percentage                        | SHP        |  
| Short-Handed Goals                         | SHG        |  
| Shots                                      | S          |  
| Shots Against                              | SAG        |  
| Shutouts                                   | SHO        |  
| Ties plus OT/SO Losses                     | TOL        |  
| Total Goals On-Ice Against                 | TGAI       |  
| Total Goals On-Ice For                     | TGFI       |  
| Wins                                       | W          |  

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/
```
<a name="league_leaders_{year}/stat_abbrev/{stat_abbrev}"></a>
### 2.2 Get player leaders by year and specific stat
- **Endpoint:** `/league_leaders_{year}/stat_abbrev/{stat_abbrev}`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and specific category.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{stat_abbrev}`** (string) - Short abbreviation of categories.
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`stat_name`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL"). Sometimes you can see the values ​​2TM, 3TM, etc. 2TM means the player played for 2 teams, 3TM - for three teams, etc.
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`stat_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:  

    
| Stat name                                   | Short code |  
|---------------------------------------------|------------|  
| Assists                                    | A          |  
| Assists Per Game                           | APG        |  
| Defensive Point Shares                     | DPS        |  
| Even Strength Goals                        | EVSG       |  
| Expected +/-                               | XPM        |  
| Game-Winning Goals                         | GWG        |  
| Games Played (Goalie)                      | GPG        |  
| Goalie Point Shares                        | GPS        |  
| Goals                                      | G          |  
| Goals Against                              | GA         |  
| Goals Against Average                      | GAA        |  
| Goals Allowed Adjusted                     | GAAJ       |  
| Goals Created                              | GCR        |  
| Goals Created Per Game                     | GCPG       |  
| Goals Per Game                             | GPGM       |  
| Goals Saved Above Average                  | GSAA       |  
| Hat Tricks                                 | HTR        |  
| Losses                                     | L          |  
| Minutes                                    | MIN        |  
| Offensive Point Shares                     | OPS        |  
| Penalties in Minutes                       | PIM        |  
| Plus/Minus                                 | PLM        |  
| Point Shares                               | PTS        |  
| Points                                     | P          |  
| Points Per Game                            | PPG        |  
| Power Play Goals                           | PPGL       |  
| Power Play Goals On-Ice Against            | PGAI       |  
| Power Play Goals On-Ice For                | PGFI       |  
| Save Percentage                            | SVP        |  
| Saves                                      | SAV        |  
| Shooting Percentage                        | SHP        |  
| Short-Handed Goals                         | SHG        |  
| Shots                                      | S          |  
| Shots Against                              | SAG        |  
| Shutouts                                   | SHO        |  
| Ties plus OT/SO Losses                     | TOL        |  
| Total Goals On-Ice Against                 | TGAI       |  
| Total Goals On-Ice For                     | TGFI       |  
| Wins                                       | W          |  


##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/stat_abbrev/GPS/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/stat_abbrev/GPS/
```
<a name="league_leaders_{year}/stat_abbrev/{stat_abbrev}/rank/{rank}"></a>
### 2.3 Get player leaders by year and specific stat and rank
- **Endpoint:** `/league_leaders_{year}/stat_abbrev/{stat_abbrev}/rank/{rank}`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and specific category and rank.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{stat_abbrev}`** (string) - Short abbreviation of categories.
   - **`{rank}`** (string) - Rank in the leaderboard, first place is the best.
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`stat_name`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL"). Sometimes you can see the values ​​2TM, 3TM, etc. 2TM means the player played for 2 teams, 3TM - for three teams, etc.
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`stat_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:  

    
| Stat name                                   | Short code |  
|---------------------------------------------|------------|  
| Assists                                    | A          |  
| Assists Per Game                           | APG        |  
| Defensive Point Shares                     | DPS        |  
| Even Strength Goals                        | EVSG       |  
| Expected +/-                               | XPM        |  
| Game-Winning Goals                         | GWG        |  
| Games Played (Goalie)                      | GPG        |  
| Goalie Point Shares                        | GPS        |  
| Goals                                      | G          |  
| Goals Against                              | GA         |  
| Goals Against Average                      | GAA        |  
| Goals Allowed Adjusted                     | GAAJ       |  
| Goals Created                              | GCR        |  
| Goals Created Per Game                     | GCPG       |  
| Goals Per Game                             | GPGM       |  
| Goals Saved Above Average                  | GSAA       |  
| Hat Tricks                                 | HTR        |  
| Losses                                     | L          |  
| Minutes                                    | MIN        |  
| Offensive Point Shares                     | OPS        |  
| Penalties in Minutes                       | PIM        |  
| Plus/Minus                                 | PLM        |  
| Point Shares                               | PTS        |  
| Points                                     | P          |  
| Points Per Game                            | PPG        |  
| Power Play Goals                           | PPGL       |  
| Power Play Goals On-Ice Against            | PGAI       |  
| Power Play Goals On-Ice For                | PGFI       |  
| Save Percentage                            | SVP        |  
| Saves                                      | SAV        |  
| Shooting Percentage                        | SHP        |  
| Short-Handed Goals                         | SHG        |  
| Shots                                      | S          |  
| Shots Against                              | SAG        |  
| Shutouts                                   | SHO        |  
| Ties plus OT/SO Losses                     | TOL        |  
| Total Goals On-Ice Against                 | TGAI       |  
| Total Goals On-Ice For                     | TGFI       |  
| Wins                                       | W          |  

##### Example by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/stat_abbrev/GPS/rank/3/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/stat_abbrev/GPS/rank/3/
```
<a name="league_leaders_{year}/stat_abbrev/{stat_abbrev}/player_id/{player_id}"></a>
### 2.4 Get player leaders by year and specific stat and player ID
- **Endpoint:** `/league_leaders_{year}/stat_abbrev/{stat_abbrev}/player_id/{player_id}`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and specific category and player ID.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{stat_abbrev}`** (string) - Short abbreviation of categories.
   - **`{player_id}`** (string) - Unique identifier for each player, contains letters and numbers.
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`stat_name`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL"). Sometimes you can see the values ​​2TM, 3TM, etc. 2TM means the player played for 2 teams, 3TM - for three teams, etc.
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`stat_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:  

    
| Stat name                                   | Short code |  
|---------------------------------------------|------------|  
| Assists                                    | A          |  
| Assists Per Game                           | APG        |  
| Defensive Point Shares                     | DPS        |  
| Even Strength Goals                        | EVSG       |  
| Expected +/-                               | XPM        |  
| Game-Winning Goals                         | GWG        |  
| Games Played (Goalie)                      | GPG        |  
| Goalie Point Shares                        | GPS        |  
| Goals                                      | G          |  
| Goals Against                              | GA         |  
| Goals Against Average                      | GAA        |  
| Goals Allowed Adjusted                     | GAAJ       |  
| Goals Created                              | GCR        |  
| Goals Created Per Game                     | GCPG       |  
| Goals Per Game                             | GPGM       |  
| Goals Saved Above Average                  | GSAA       |  
| Hat Tricks                                 | HTR        |  
| Losses                                     | L          |  
| Minutes                                    | MIN        |  
| Offensive Point Shares                     | OPS        |  
| Penalties in Minutes                       | PIM        |  
| Plus/Minus                                 | PLM        |  
| Point Shares                               | PTS        |  
| Points                                     | P          |  
| Points Per Game                            | PPG        |  
| Power Play Goals                           | PPGL       |  
| Power Play Goals On-Ice Against            | PGAI       |  
| Power Play Goals On-Ice For                | PGFI       |  
| Save Percentage                            | SVP        |  
| Saves                                      | SAV        |  
| Shooting Percentage                        | SHP        |  
| Short-Handed Goals                         | SHG        |  
| Shots                                      | S          |  
| Shots Against                              | SAG        |  
| Shutouts                                   | SHO        |  
| Ties plus OT/SO Losses                     | TOL        |  
| Total Goals On-Ice Against                 | TGAI       |  
| Total Goals On-Ice For                     | TGFI       |  
| Wins                                       | W          |  

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/stat_abbrev/GPS/player_id/vasilan02/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/stat_abbrev/GPS/player_id/vasilan02/
```
<a name="league_leaders_{year}/stat_abbrev/{stat_abbrev}/team_abbrev/{team_abbrev}"></a>
### 2.5 Get player leaders by year and specific stat and team
- **Endpoint:** `/league_leaders_{year}/stat_abbrev/{stat_abbrev}/team_abbrev/{team_abbrev}`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and specific category and team.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{stat_abbrev}`** (string) - Short abbreviation of categories.
   - **`{team_abbrev}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`stat_name`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL"). Sometimes you can see the values ​​2TM, 3TM, etc. 2TM means the player played for 2 teams, 3TM - for three teams, etc.
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`stat_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:  

    
| Stat name                                   | Short code |  
|---------------------------------------------|------------|  
| Assists                                    | A          |  
| Assists Per Game                           | APG        |  
| Defensive Point Shares                     | DPS        |  
| Even Strength Goals                        | EVSG       |  
| Expected +/-                               | XPM        |  
| Game-Winning Goals                         | GWG        |  
| Games Played (Goalie)                      | GPG        |  
| Goalie Point Shares                        | GPS        |  
| Goals                                      | G          |  
| Goals Against                              | GA         |  
| Goals Against Average                      | GAA        |  
| Goals Allowed Adjusted                     | GAAJ       |  
| Goals Created                              | GCR        |  
| Goals Created Per Game                     | GCPG       |  
| Goals Per Game                             | GPGM       |  
| Goals Saved Above Average                  | GSAA       |  
| Hat Tricks                                 | HTR        |  
| Losses                                     | L          |  
| Minutes                                    | MIN        |  
| Offensive Point Shares                     | OPS        |  
| Penalties in Minutes                       | PIM        |  
| Plus/Minus                                 | PLM        |  
| Point Shares                               | PTS        |  
| Points                                     | P          |  
| Points Per Game                            | PPG        |  
| Power Play Goals                           | PPGL       |  
| Power Play Goals On-Ice Against            | PGAI       |  
| Power Play Goals On-Ice For                | PGFI       |  
| Save Percentage                            | SVP        |  
| Saves                                      | SAV        |  
| Shooting Percentage                        | SHP        |  
| Short-Handed Goals                         | SHG        |  
| Shots                                      | S          |  
| Shots Against                              | SAG        |  
| Shutouts                                   | SHO        |  
| Ties plus OT/SO Losses                     | TOL        |  
| Total Goals On-Ice Against                 | TGAI       |  
| Total Goals On-Ice For                     | TGFI       |  
| Wins                                       | W          |  

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/stat_abbrev/GPS/team_abbrev/TBL/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/stat_abbrev/GPS/team_abbrev/TBL/
```
<a name="league_leaders_{year}/rank/{rank}"></a>
### 2.6 Get player leaders by year and specific rank
- **Endpoint:** `/league_leaders_{year}/rank/{rank}`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and specific rank.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{rank}`** (integer) - Rank in the leaderboard, first place is the best.
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`stat_name`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL"). Sometimes you can see the values ​​2TM, 3TM, etc. 2TM means the player played for 2 teams, 3TM - for three teams, etc.
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`stat_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:  

    
| Stat name                                   | Short code |  
|---------------------------------------------|------------|  
| Assists                                    | A          |  
| Assists Per Game                           | APG        |  
| Defensive Point Shares                     | DPS        |  
| Even Strength Goals                        | EVSG       |  
| Expected +/-                               | XPM        |  
| Game-Winning Goals                         | GWG        |  
| Games Played (Goalie)                      | GPG        |  
| Goalie Point Shares                        | GPS        |  
| Goals                                      | G          |  
| Goals Against                              | GA         |  
| Goals Against Average                      | GAA        |  
| Goals Allowed Adjusted                     | GAAJ       |  
| Goals Created                              | GCR        |  
| Goals Created Per Game                     | GCPG       |  
| Goals Per Game                             | GPGM       |  
| Goals Saved Above Average                  | GSAA       |  
| Hat Tricks                                 | HTR        |  
| Losses                                     | L          |  
| Minutes                                    | MIN        |  
| Offensive Point Shares                     | OPS        |  
| Penalties in Minutes                       | PIM        |  
| Plus/Minus                                 | PLM        |  
| Point Shares                               | PTS        |  
| Points                                     | P          |  
| Points Per Game                            | PPG        |  
| Power Play Goals                           | PPGL       |  
| Power Play Goals On-Ice Against            | PGAI       |  
| Power Play Goals On-Ice For                | PGFI       |  
| Save Percentage                            | SVP        |  
| Saves                                      | SAV        |  
| Shooting Percentage                        | SHP        |  
| Short-Handed Goals                         | SHG        |  
| Shots                                      | S          |  
| Shots Against                              | SAG        |  
| Shutouts                                   | SHO        |  
| Ties plus OT/SO Losses                     | TOL        |  
| Total Goals On-Ice Against                 | TGAI       |  
| Total Goals On-Ice For                     | TGFI       |  
| Wins                                       | W          |  

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/rank/3/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/rank/3/
```
<a name="league_leaders_{year}/rank/{rank}/player_id/{player_id}"></a>
### 2.7 Get player leaders by year and specific rank and player ID
- **Endpoint:** `/league_leaders_{year}/rank/{rank}/player_id/{player_id}`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and specific rank and player ID.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{rank}`** (integer) - Rank in the leaderboard, first place is the best.
   - **`{player_id}`** (string) - Unique identifier for each player, contains letters and numbers.
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`stat_name`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL"). Sometimes you can see the values ​​2TM, 3TM, etc. 2TM means the player played for 2 teams, 3TM - for three teams, etc.
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`stat_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:  

    
| Stat name                                   | Short code |  
|---------------------------------------------|------------|  
| Assists                                    | A          |  
| Assists Per Game                           | APG        |  
| Defensive Point Shares                     | DPS        |  
| Even Strength Goals                        | EVSG       |  
| Expected +/-                               | XPM        |  
| Game-Winning Goals                         | GWG        |  
| Games Played (Goalie)                      | GPG        |  
| Goalie Point Shares                        | GPS        |  
| Goals                                      | G          |  
| Goals Against                              | GA         |  
| Goals Against Average                      | GAA        |  
| Goals Allowed Adjusted                     | GAAJ       |  
| Goals Created                              | GCR        |  
| Goals Created Per Game                     | GCPG       |  
| Goals Per Game                             | GPGM       |  
| Goals Saved Above Average                  | GSAA       |  
| Hat Tricks                                 | HTR        |  
| Losses                                     | L          |  
| Minutes                                    | MIN        |  
| Offensive Point Shares                     | OPS        |  
| Penalties in Minutes                       | PIM        |  
| Plus/Minus                                 | PLM        |  
| Point Shares                               | PTS        |  
| Points                                     | P          |  
| Points Per Game                            | PPG        |  
| Power Play Goals                           | PPGL       |  
| Power Play Goals On-Ice Against            | PGAI       |  
| Power Play Goals On-Ice For                | PGFI       |  
| Save Percentage                            | SVP        |  
| Saves                                      | SAV        |  
| Shooting Percentage                        | SHP        |  
| Short-Handed Goals                         | SHG        |  
| Shots                                      | S          |  
| Shots Against                              | SAG        |  
| Shutouts                                   | SHO        |  
| Ties plus OT/SO Losses                     | TOL        |  
| Total Goals On-Ice Against                 | TGAI       |  
| Total Goals On-Ice For                     | TGFI       |  
| Wins                                       | W          |  

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/rank/3/player_id/marksja02/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/rank/3/player_id/kuempda01/
```
<a name="league_leaders_{year}/rank/{rank}/team_abbrev/{team_abbrev}"></a>
### 2.8 Get player leaders by year and specific rank and team
- **Endpoint:** `/league_leaders_{year}/rank/{rank}/team_abbrev/{team_abbrev}`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and specific rank and team.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{rank}`** (integer) - Rank in the leaderboard, first place is the best.
   - **`{team_abbrev}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`stat_name`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL"). Sometimes you can see the values ​​2TM, 3TM, etc. 2TM means the player played for 2 teams, 3TM - for three teams, etc.
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`stat_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:  
    
| Stat name                                   | Short code |  
|---------------------------------------------|------------|  
| Assists                                    | A          |  
| Assists Per Game                           | APG        |  
| Defensive Point Shares                     | DPS        |  
| Even Strength Goals                        | EVSG       |  
| Expected +/-                               | XPM        |  
| Game-Winning Goals                         | GWG        |  
| Games Played (Goalie)                      | GPG        |  
| Goalie Point Shares                        | GPS        |  
| Goals                                      | G          |  
| Goals Against                              | GA         |  
| Goals Against Average                      | GAA        |  
| Goals Allowed Adjusted                     | GAAJ       |  
| Goals Created                              | GCR        |  
| Goals Created Per Game                     | GCPG       |  
| Goals Per Game                             | GPGM       |  
| Goals Saved Above Average                  | GSAA       |  
| Hat Tricks                                 | HTR        |  
| Losses                                     | L          |  
| Minutes                                    | MIN        |  
| Offensive Point Shares                     | OPS        |  
| Penalties in Minutes                       | PIM        |  
| Plus/Minus                                 | PLM        |  
| Point Shares                               | PTS        |  
| Points                                     | P          |  
| Points Per Game                            | PPG        |  
| Power Play Goals                           | PPGL       |  
| Power Play Goals On-Ice Against            | PGAI       |  
| Power Play Goals On-Ice For                | PGFI       |  
| Save Percentage                            | SVP        |  
| Saves                                      | SAV        |  
| Shooting Percentage                        | SHP        |  
| Short-Handed Goals                         | SHG        |  
| Shots                                      | S          |  
| Shots Against                              | SAG        |  
| Shutouts                                   | SHO        |  
| Ties plus OT/SO Losses                     | TOL        |  
| Total Goals On-Ice Against                 | TGAI       |  
| Total Goals On-Ice For                     | TGFI       |  
| Wins                                       | W          |  

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/rank/3/team_abbrev/TBL/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/rank/3/team_abbrev/TBL/
```
<a name="league_leaders_{year}/player_id/{player_id}"></a>
### 2.9 Get player leaders by year and specific player ID
- **Endpoint:** `/league_leaders_{year}/player_id/{player_id}`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and specific player ID.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{player_id}`** (string) - Unique identifier for each player, contains letters and numbers.
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`stat_name`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL"). Sometimes you can see the values ​​2TM, 3TM, etc. 2TM means the player played for 2 teams, 3TM - for three teams, etc.
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`stat_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:  
    
| Stat name                                   | Short code |  
|---------------------------------------------|------------|  
| Assists                                    | A          |  
| Assists Per Game                           | APG        |  
| Defensive Point Shares                     | DPS        |  
| Even Strength Goals                        | EVSG       |  
| Expected +/-                               | XPM        |  
| Game-Winning Goals                         | GWG        |  
| Games Played (Goalie)                      | GPG        |  
| Goalie Point Shares                        | GPS        |  
| Goals                                      | G          |  
| Goals Against                              | GA         |  
| Goals Against Average                      | GAA        |  
| Goals Allowed Adjusted                     | GAAJ       |  
| Goals Created                              | GCR        |  
| Goals Created Per Game                     | GCPG       |  
| Goals Per Game                             | GPGM       |  
| Goals Saved Above Average                  | GSAA       |  
| Hat Tricks                                 | HTR        |  
| Losses                                     | L          |  
| Minutes                                    | MIN        |  
| Offensive Point Shares                     | OPS        |  
| Penalties in Minutes                       | PIM        |  
| Plus/Minus                                 | PLM        |  
| Point Shares                               | PTS        |  
| Points                                     | P          |  
| Points Per Game                            | PPG        |  
| Power Play Goals                           | PPGL       |  
| Power Play Goals On-Ice Against            | PGAI       |  
| Power Play Goals On-Ice For                | PGFI       |  
| Save Percentage                            | SVP        |  
| Saves                                      | SAV        |  
| Shooting Percentage                        | SHP        |  
| Short-Handed Goals                         | SHG        |  
| Shots                                      | S          |  
| Shots Against                              | SAG        |  
| Shutouts                                   | SHO        |  
| Ties plus OT/SO Losses                     | TOL        |  
| Total Goals On-Ice Against                 | TGAI       |  
| Total Goals On-Ice For                     | TGFI       |  
| Wins                                       | W          |  

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/player_id/kreidch01/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/player_id/kreidch01/
```
<a name="league_leaders_{year}/team_abbrev/{team_abbrev}"></a>
### 2.10 Get player leaders by year and specific team
- **Endpoint:** `/league_leaders_{year}/team_abbrev/{team_abbrev}`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and specific team.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{team_abbrev}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`stat_name`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL"). Sometimes you can see the values ​​2TM, 3TM, etc. 2TM means the player played for 2 teams, 3TM - for three teams, etc.
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`stat_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code: 
    
| Stat name                                   | Short code |  
|---------------------------------------------|------------|  
| Assists                                    | A          |  
| Assists Per Game                           | APG        |  
| Defensive Point Shares                     | DPS        |  
| Even Strength Goals                        | EVSG       |  
| Expected +/-                               | XPM        |  
| Game-Winning Goals                         | GWG        |  
| Games Played (Goalie)                      | GPG        |  
| Goalie Point Shares                        | GPS        |  
| Goals                                      | G          |  
| Goals Against                              | GA         |  
| Goals Against Average                      | GAA        |  
| Goals Allowed Adjusted                     | GAAJ       |  
| Goals Created                              | GCR        |  
| Goals Created Per Game                     | GCPG       |  
| Goals Per Game                             | GPGM       |  
| Goals Saved Above Average                  | GSAA       |  
| Hat Tricks                                 | HTR        |  
| Losses                                     | L          |  
| Minutes                                    | MIN        |  
| Offensive Point Shares                     | OPS        |  
| Penalties in Minutes                       | PIM        |  
| Plus/Minus                                 | PLM        |  
| Point Shares                               | PTS        |  
| Points                                     | P          |  
| Points Per Game                            | PPG        |  
| Power Play Goals                           | PPGL       |  
| Power Play Goals On-Ice Against            | PGAI       |  
| Power Play Goals On-Ice For                | PGFI       |  
| Save Percentage                            | SVP        |  
| Saves                                      | SAV        |  
| Shooting Percentage                        | SHP        |  
| Short-Handed Goals                         | SHG        |  
| Shots                                      | S          |  
| Shots Against                              | SAG        |  
| Shutouts                                   | SHO        |  
| Ties plus OT/SO Losses                     | TOL        |  
| Total Goals On-Ice Against                 | TGAI       |  
| Total Goals On-Ice For                     | TGFI       |  
| Wins                                       | W          |  

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/team_abbrev/TOR/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/team_abbrev/TOR/
```
<a name="league_leaders_{year}/team_abbrev/{team_abbrev}/player_id/{player_id}"></a>
### 2.11 Get player leaders by year and specific team and player ID
- **Endpoint:** `/league_leaders_{year}/team_abbrev/{team_abbrev}/player_id/{player_id}`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and specific team and player ID.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{team_abbrev}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
   - **`{player_id}`** (string) - Unique identifier for each player, contains letters and numbers.
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`stat_name`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL"). Sometimes you can see the values ​​2TM, 3TM, etc. 2TM means the player played for 2 teams, 3TM - for three teams, etc.
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`stat_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:  
    
| Stat name                                   | Short code |  
|---------------------------------------------|------------|  
| Assists                                    | A          |  
| Assists Per Game                           | APG        |  
| Defensive Point Shares                     | DPS        |  
| Even Strength Goals                        | EVSG       |  
| Expected +/-                               | XPM        |  
| Game-Winning Goals                         | GWG        |  
| Games Played (Goalie)                      | GPG        |  
| Goalie Point Shares                        | GPS        |  
| Goals                                      | G          |  
| Goals Against                              | GA         |  
| Goals Against Average                      | GAA        |  
| Goals Allowed Adjusted                     | GAAJ       |  
| Goals Created                              | GCR        |  
| Goals Created Per Game                     | GCPG       |  
| Goals Per Game                             | GPGM       |  
| Goals Saved Above Average                  | GSAA       |  
| Hat Tricks                                 | HTR        |  
| Losses                                     | L          |  
| Minutes                                    | MIN        |  
| Offensive Point Shares                     | OPS        |  
| Penalties in Minutes                       | PIM        |  
| Plus/Minus                                 | PLM        |  
| Point Shares                               | PTS        |  
| Points                                     | P          |  
| Points Per Game                            | PPG        |  
| Power Play Goals                           | PPGL       |  
| Power Play Goals On-Ice Against            | PGAI       |  
| Power Play Goals On-Ice For                | PGFI       |  
| Save Percentage                            | SVP        |  
| Saves                                      | SAV        |  
| Shooting Percentage                        | SHP        |  
| Short-Handed Goals                         | SHG        |  
| Shots                                      | S          |  
| Shots Against                              | SAG        |  
| Shutouts                                   | SHO        |  
| Ties plus OT/SO Losses                     | TOL        |  
| Total Goals On-Ice Against                 | TGAI       |  
| Total Goals On-Ice For                     | TGFI       |  
| Wins                                       | W          |  

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/team_abbrev/TOR/player_id/matthau01/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/team_abbrev/TOR/player_id/matthau01/
```
<a name="basic_stats_players_regular_season_{year}"></a>
### 2.12 Get basic stats players regular season by year
- **Endpoint:** `/basic_stats_players_regular_season_{year}/`
- **Method:** GET
- **Description:** Returns a table of basic individual player statistics for the specified NHL regular season. Each object represents a player’s statistical profile for that season. For seasons from 2007–08 onward, contains additional columns such as total shot attempts and faceoff stats..
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`goals`** (integer) - Goals scored.
  - **`goals_per_game`** (number, decimal) - Goals per game (goals/games_played).
  - **`assists`** (integer) - Assists.
  - **`assists_per_game`** (number, decimal) - Assists per game (assists/games_played).
  - **`points`** (integer) - Points (Goals + Assists).
  - **`points_per_game`** (number, decimal) - Points per game (points/games_played).
  - **`xpm`** (integer) - Plus/Minus Rating (net difference in goals scored and allowed on the ice with this player's participation).
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game (xpm/games_played).
  - **`pim`** (integer) - Penalties in Minutes — total penalty minutes accrued.
  - **`pim_per_game`** (number, decimal) - Penalty minutes per game. (pim/games_played).
  - **`evsg`** (integer) - Even Strength Goals.
  - **`evsg_per_game`** (number, decimal) - Even strength goals per game (evsg/games_played).
  - **`ppgl`** (integer) - Power Play Goals — goals scored with man advantage.
  - **`ppgl_per_game`** (number, decimal) - Power play goals per game. (ppgl/games_played).
  - **`shg`** (integer) - Short-handed Goals — goals scored when team is short-handed.
  - **`shg_per_game`** (number, decimal) - Short-handed goals per game. (shg/games_played).
  - **`gwg`** (integer) - Game-Winning Goals.
  - **`gwg_per_game`** (number, decimal) - Game-winning goals per game. (gwg/games_played).
  - **`evsa`** (integer) - Even Strength Assists — assists at even strength.
  - **`evsa_per_game`** (number, decimal) - Even strength assists per game. (evsa/games_played).
  - **`ppa`** (integer) - Power Play Assists — assists on power play goals.
  - **`ppa_per_game`** (number, decimal) - Power play assists per game. (ppa/games_played).
  - **`sha`** (integer) - Short-handed Assists — assists while team is short-handed.
  - **`sha_per_game`** (number, decimal) - Short-handed assists per game. (sha/games_played).
  - **`sog`** (integer) - Shots on Goal.
  - **`sog_per_game`** (number, decimal) - Shots on goal per game. (sog/games_played).
  - **`shp`** (number, decimal) - Shooting percentage, as a number (typically XX.X). No percent sign.
  - **`shp_decimal`** (number, decimal) - Shooting percentage, as a decimal fraction (e.g., 12.6% → 0.126).
  - **`toi`** (string) - Total time on ice for the season — expressed as mm:ss.
  - **`toi_decimal`** (number, decimal) - Total time on ice, as decimal minutes.
  - **`atoi`** (string) - Average time on ice per game (mm:ss).
  - **`atoi_decimal`** (number, decimal) - Average time on ice per game, decimal minutes.
  - **`tsa`** (integer) - Total Shot Attempts (2007–08 and later season).
  - **`tsa_per_game`** (number, decimal) - Total Shot Attempts per game. (tsa/games_played) (2007–08 and later season).
  - **`fow`** (integer) - Faceoff Wins (2007–08 and later season).
  - **`fow_per_game`** (number, decimal) - Faceoff Wins per game. (fow/games_played) (2007–08 and later season).
  - **`fol`** (integer) - Faceoff Losses (2007–08 and later season).
  - **`fol_per_game`** (number, decimal) - Faceoff Losses per game. (fol/games_played) (2007–08 and later season).
  - **`fo_per`** (number, decimal) - Faceoff Win Percentage, as percent (e.g., 52.1). (2007–08 and later season).
  - **`fol_per_decimal`** (number, decimal) - Faceoff win rate, decimal (e.g., 0.521). (2007–08 and later season).
  - **`blk`** (integer) - Blocked Shots: number of opponent shots blocked. (2007–08 and later season).
  - **`blk_per_game`** (number, decimal) - Blocked shots per game. (blk/games_played) (2007–08 and later season).
  - **`hit`** (integer) - Hits. (2007–08 and later season).
  - **`hit_per_game`** (number, decimal) - Hits per game. (hit/games_played) (2007–08 and later season).
  - **`take`** (integer) - Takeaways. (2007–08 and later season).
  - **`tak_per_game`** (number, decimal) - Takeaways per game. (take/games_played) (2007–08 and later season).
  - **`give`** (integer) - Giveaways. (2007–08 and later season).
  - **`give_per_game`** (number, decimal) - Giveaways per game. (give/games_played) (2007–08 and later season).
  - **`awards`** (string) - List of any individual awards received.
    
> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played.**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_regular_season_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_regular_season_now/
```
<a name="basic_stats_players_regular_season_{year}/rank/{rank}"></a>
### 2.13 Get basic stats players regular season by year and specific rank
- **Endpoint:** `/basic_stats_players_regular_season_{year}/rank/{rank}/`
- **Method:** GET
- **Description:** Returns a table of basic individual player statistics for the specified NHL regular season by rank. Each object represents a player’s statistical profile for that season. For seasons from 2007–08 onward, contains additional columns such as total shot attempts and faceoff stats.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`goals`** (integer) - Goals scored.
  - **`goals_per_game`** (number, decimal) - Goals per game (goals/games_played).
  - **`assists`** (integer) - Assists.
  - **`assists_per_game`** (number, decimal) - Assists per game (assists/games_played).
  - **`points`** (integer) - Points (Goals + Assists).
  - **`points_per_game`** (number, decimal) - Points per game (points/games_played).
  - **`xpm`** (integer) - Plus/Minus Rating (net difference in goals scored and allowed on the ice with this player's participation).
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game (xpm/games_played).
  - **`pim`** (integer) - Penalties in Minutes — total penalty minutes accrued.
  - **`pim_per_game`** (number, decimal) - Penalty minutes per game. (pim/games_played).
  - **`evsg`** (integer) - Even Strength Goals.
  - **`evsg_per_game`** (number, decimal) - Even strength goals per game (evsg/games_played).
  - **`ppgl`** (integer) - Power Play Goals — goals scored with man advantage.
  - **`ppgl_per_game`** (number, decimal) - Power play goals per game. (ppgl/games_played).
  - **`shg`** (integer) - Short-handed Goals — goals scored when team is short-handed.
  - **`shg_per_game`** (number, decimal) - Short-handed goals per game. (shg/games_played).
  - **`gwg`** (integer) - Game-Winning Goals.
  - **`gwg_per_game`** (number, decimal) - Game-winning goals per game. (gwg/games_played).
  - **`evsa`** (integer) - Even Strength Assists — assists at even strength.
  - **`evsa_per_game`** (number, decimal) - Even strength assists per game. (evsa/games_played).
  - **`ppa`** (integer) - Power Play Assists — assists on power play goals.
  - **`ppa_per_game`** (number, decimal) - Power play assists per game. (ppa/games_played).
  - **`sha`** (integer) - Short-handed Assists — assists while team is short-handed.
  - **`sha_per_game`** (number, decimal) - Short-handed assists per game. (sha/games_played).
  - **`sog`** (integer) - Shots on Goal.
  - **`sog_per_game`** (number, decimal) - Shots on goal per game. (sog/games_played).
  - **`shp`** (number, decimal) - Shooting percentage, as a number (typically XX.X). No percent sign.
  - **`shp_decimal`** (number, decimal) - Shooting percentage, as a decimal fraction (e.g., 12.6% → 0.126).
  - **`toi`** (string) - Total time on ice for the season — expressed as mm:ss.
  - **`toi_decimal`** (number, decimal) - Total time on ice, as decimal minutes.
  - **`atoi`** (string) - Average time on ice per game (mm:ss).
  - **`atoi_decimal`** (number, decimal) - Average time on ice per game, decimal minutes.
  - **`tsa`** (integer) - Total Shot Attempts (2007–08 and later season).
  - **`tsa_per_game`** (number, decimal) - Total Shot Attempts per game. (tsa/games_played) (2007–08 and later season).
  - **`fow`** (integer) - Faceoff Wins (2007–08 and later season).
  - **`fow_per_game`** (number, decimal) - Faceoff Wins per game. (fow/games_played) (2007–08 and later season).
  - **`fol`** (integer) - Faceoff Losses (2007–08 and later season).
  - **`fol_per_game`** (number, decimal) - Faceoff Losses per game. (fol/games_played) (2007–08 and later season).
  - **`fo_per`** (number, decimal) - Faceoff Win Percentage, as percent (e.g., 52.1). (2007–08 and later season).
  - **`fol_per_decimal`** (number, decimal) - Faceoff win rate, decimal (e.g., 0.521). (2007–08 and later season).
  - **`blk`** (integer) - Blocked Shots: number of opponent shots blocked. (2007–08 and later season).
  - **`blk_per_game`** (number, decimal) - Blocked shots per game. (blk/games_played) (2007–08 and later season).
  - **`hit`** (integer) - Hits. (2007–08 and later season).
  - **`hit_per_game`** (number, decimal) - Hits per game. (hit/games_played) (2007–08 and later season).
  - **`take`** (integer) - Takeaways. (2007–08 and later season).
  - **`tak_per_game`** (number, decimal) - Takeaways per game. (take/games_played) (2007–08 and later season).
  - **`give`** (integer) - Giveaways. (2007–08 and later season).
  - **`give_per_game`** (number, decimal) - Giveaways per game. (give/games_played) (2007–08 and later season).
  - **`awards`** (string) - List of any individual awards received.

> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played.**
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_regular_season_20212022/rank/17
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_regular_season_now/rank/17
```
<a name="basic_stats_players_regular_season_{year}/team_abbrev/{team_abbrev}"></a>
### 2.14 Get basic stats players regular season by year and specific team
- **Endpoint:** `/basic_stats_players_regular_season_{year}/team_abbrev/{team_abbrev}/`
- **Method:** GET
- **Description:** Returns a table of basic individual player statistics for the specified NHL regular season by team. Each object represents a player’s statistical profile for that season. For seasons from 2007–08 onward, contains additional columns such as total shot attempts and faceoff stats.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`goals`** (integer) - Goals scored.
  - **`goals_per_game`** (number, decimal) - Goals per game (goals/games_played).
  - **`assists`** (integer) - Assists.
  - **`assists_per_game`** (number, decimal) - Assists per game (assists/games_played).
  - **`points`** (integer) - Points (Goals + Assists).
  - **`points_per_game`** (number, decimal) - Points per game (points/games_played).
  - **`xpm`** (integer) - Plus/Minus Rating (net difference in goals scored and allowed on the ice with this player's participation).
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game (xpm/games_played).
  - **`pim`** (integer) - Penalties in Minutes — total penalty minutes accrued.
  - **`pim_per_game`** (number, decimal) - Penalty minutes per game. (pim/games_played).
  - **`evsg`** (integer) - Even Strength Goals.
  - **`evsg_per_game`** (number, decimal) - Even strength goals per game (evsg/games_played).
  - **`ppgl`** (integer) - Power Play Goals — goals scored with man advantage.
  - **`ppgl_per_game`** (number, decimal) - Power play goals per game. (ppgl/games_played).
  - **`shg`** (integer) - Short-handed Goals — goals scored when team is short-handed.
  - **`shg_per_game`** (number, decimal) - Short-handed goals per game. (shg/games_played).
  - **`gwg`** (integer) - Game-Winning Goals.
  - **`gwg_per_game`** (number, decimal) - Game-winning goals per game. (gwg/games_played).
  - **`evsa`** (integer) - Even Strength Assists — assists at even strength.
  - **`evsa_per_game`** (number, decimal) - Even strength assists per game. (evsa/games_played).
  - **`ppa`** (integer) - Power Play Assists — assists on power play goals.
  - **`ppa_per_game`** (number, decimal) - Power play assists per game. (ppa/games_played).
  - **`sha`** (integer) - Short-handed Assists — assists while team is short-handed.
  - **`sha_per_game`** (number, decimal) - Short-handed assists per game. (sha/games_played).
  - **`sog`** (integer) - Shots on Goal.
  - **`sog_per_game`** (number, decimal) - Shots on goal per game. (sog/games_played).
  - **`shp`** (number, decimal) - Shooting percentage, as a number (typically XX.X). No percent sign.
  - **`shp_decimal`** (number, decimal) - Shooting percentage, as a decimal fraction (e.g., 12.6% → 0.126).
  - **`toi`** (string) - Total time on ice for the season — expressed as mm:ss.
  - **`toi_decimal`** (number, decimal) - Total time on ice, as decimal minutes.
  - **`atoi`** (string) - Average time on ice per game (mm:ss).
  - **`atoi_decimal`** (number, decimal) - Average time on ice per game, decimal minutes.
  - **`tsa`** (integer) - Total Shot Attempts (2007–08 and later season).
  - **`tsa_per_game`** (number, decimal) - Total Shot Attempts per game. (tsa/games_played) (2007–08 and later season).
  - **`fow`** (integer) - Faceoff Wins (2007–08 and later season).
  - **`fow_per_game`** (number, decimal) - Faceoff Wins per game. (fow/games_played) (2007–08 and later season).
  - **`fol`** (integer) - Faceoff Losses (2007–08 and later season).
  - **`fol_per_game`** (number, decimal) - Faceoff Losses per game. (fol/games_played) (2007–08 and later season).
  - **`fo_per`** (number, decimal) - Faceoff Win Percentage, as percent (e.g., 52.1). (2007–08 and later season).
  - **`fol_per_decimal`** (number, decimal) - Faceoff win rate, decimal (e.g., 0.521). (2007–08 and later season).
  - **`blk`** (integer) - Blocked Shots: number of opponent shots blocked. (2007–08 and later season).
  - **`blk_per_game`** (number, decimal) - Blocked shots per game. (blk/games_played) (2007–08 and later season).
  - **`hit`** (integer) - Hits. (2007–08 and later season).
  - **`hit_per_game`** (number, decimal) - Hits per game. (hit/games_played) (2007–08 and later season).
  - **`take`** (integer) - Takeaways. (2007–08 and later season).
  - **`tak_per_game`** (number, decimal) - Takeaways per game. (take/games_played) (2007–08 and later season).
  - **`give`** (integer) - Giveaways. (2007–08 and later season).
  - **`give_per_game`** (number, decimal) - Giveaways per game. (give/games_played) (2007–08 and later season).
  - **`awards`** (string) - List of any individual awards received.

> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played.**
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_regular_season_20212022/team_abbrev/BOS/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_regular_season_now/team_abbrev/BOS/
```
<a name="basic_stats_players_regular_season_{year}/player_id/{player_id}"></a>
### 2.15 Get basic stats players regular season by year and player ID
- **Endpoint:** `/basic_stats_players_regular_season_{year}/player_id/{player_id}/`
- **Method:** GET
- **Description:** Returns a table of basic individual player statistics for the specified NHL regular season by player ID. Each object represents a player’s statistical profile for that season. For seasons from 2007–08 onward, contains additional columns such as total shot attempts and faceoff stats.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`goals`** (integer) - Goals scored.
  - **`goals_per_game`** (number, decimal) - Goals per game (goals/games_played).
  - **`assists`** (integer) - Assists.
  - **`assists_per_game`** (number, decimal) - Assists per game (assists/games_played).
  - **`points`** (integer) - Points (Goals + Assists).
  - **`points_per_game`** (number, decimal) - Points per game (points/games_played).
  - **`xpm`** (integer) - Plus/Minus Rating (net difference in goals scored and allowed on the ice with this player's participation).
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game (xpm/games_played).
  - **`pim`** (integer) - Penalties in Minutes — total penalty minutes accrued.
  - **`pim_per_game`** (number, decimal) - Penalty minutes per game. (pim/games_played).
  - **`evsg`** (integer) - Even Strength Goals.
  - **`evsg_per_game`** (number, decimal) - Even strength goals per game (evsg/games_played).
  - **`ppgl`** (integer) - Power Play Goals — goals scored with man advantage.
  - **`ppgl_per_game`** (number, decimal) - Power play goals per game. (ppgl/games_played).
  - **`shg`** (integer) - Short-handed Goals — goals scored when team is short-handed.
  - **`shg_per_game`** (number, decimal) - Short-handed goals per game. (shg/games_played).
  - **`gwg`** (integer) - Game-Winning Goals.
  - **`gwg_per_game`** (number, decimal) - Game-winning goals per game. (gwg/games_played).
  - **`evsa`** (integer) - Even Strength Assists — assists at even strength.
  - **`evsa_per_game`** (number, decimal) - Even strength assists per game. (evsa/games_played).
  - **`ppa`** (integer) - Power Play Assists — assists on power play goals.
  - **`ppa_per_game`** (number, decimal) - Power play assists per game. (ppa/games_played).
  - **`sha`** (integer) - Short-handed Assists — assists while team is short-handed.
  - **`sha_per_game`** (number, decimal) - Short-handed assists per game. (sha/games_played).
  - **`sog`** (integer) - Shots on Goal.
  - **`sog_per_game`** (number, decimal) - Shots on goal per game. (sog/games_played).
  - **`shp`** (number, decimal) - Shooting percentage, as a number (typically XX.X). No percent sign.
  - **`shp_decimal`** (number, decimal) - Shooting percentage, as a decimal fraction (e.g., 12.6% → 0.126).
  - **`toi`** (string) - Total time on ice for the season — expressed as mm:ss.
  - **`toi_decimal`** (number, decimal) - Total time on ice, as decimal minutes.
  - **`atoi`** (string) - Average time on ice per game (mm:ss).
  - **`atoi_decimal`** (number, decimal) - Average time on ice per game, decimal minutes.
  - **`tsa`** (integer) - Total Shot Attempts (2007–08 and later season).
  - **`tsa_per_game`** (number, decimal) - Total Shot Attempts per game. (tsa/games_played) (2007–08 and later season).
  - **`fow`** (integer) - Faceoff Wins (2007–08 and later season).
  - **`fow_per_game`** (number, decimal) - Faceoff Wins per game. (fow/games_played) (2007–08 and later season).
  - **`fol`** (integer) - Faceoff Losses (2007–08 and later season).
  - **`fol_per_game`** (number, decimal) - Faceoff Losses per game. (fol/games_played) (2007–08 and later season).
  - **`fo_per`** (number, decimal) - Faceoff Win Percentage, as percent (e.g., 52.1). (2007–08 and later season).
  - **`fol_per_decimal`** (number, decimal) - Faceoff win rate, decimal (e.g., 0.521). (2007–08 and later season).
  - **`blk`** (integer) - Blocked Shots: number of opponent shots blocked. (2007–08 and later season).
  - **`blk_per_game`** (number, decimal) - Blocked shots per game. (blk/games_played) (2007–08 and later season).
  - **`hit`** (integer) - Hits. (2007–08 and later season).
  - **`hit_per_game`** (number, decimal) - Hits per game. (hit/games_played) (2007–08 and later season).
  - **`take`** (integer) - Takeaways. (2007–08 and later season).
  - **`tak_per_game`** (number, decimal) - Takeaways per game. (take/games_played) (2007–08 and later season).
  - **`give`** (integer) - Giveaways. (2007–08 and later season).
  - **`give_per_game`** (number, decimal) - Giveaways per game. (give/games_played) (2007–08 and later season).
  - **`awards`** (string) - List of any individual awards received.

> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played.**
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_regular_season_20212022/player_id/ahose01/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_regular_season_now/player_id/ahose01/
```
<a name="basic_stats_players_regular_season_{year}/position/{position}"></a>
### 2.16 Get basic stats players regular season by year and position
- **Endpoint:** `/basic_stats_players_regular_season_{year}/position/{position}/`
- **Method:** GET
- **Description:** Returns a table of basic individual player statistics for the specified NHL regular season by position player. Each object represents a player’s statistical profile for that season. For seasons from 2007–08 onward, contains additional columns such as total shot attempts and faceoff stats.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`position`** (string) - Primary position played (C, LW, RW, D).
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`goals`** (integer) - Goals scored.
  - **`goals_per_game`** (number, decimal) - Goals per game (goals/games_played).
  - **`assists`** (integer) - Assists.
  - **`assists_per_game`** (number, decimal) - Assists per game (assists/games_played).
  - **`points`** (integer) - Points (Goals + Assists).
  - **`points_per_game`** (number, decimal) - Points per game (points/games_played).
  - **`xpm`** (integer) - Plus/Minus Rating (net difference in goals scored and allowed on the ice with this player's participation).
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game (xpm/games_played).
  - **`pim`** (integer) - Penalties in Minutes — total penalty minutes accrued.
  - **`pim_per_game`** (number, decimal) - Penalty minutes per game. (pim/games_played).
  - **`evsg`** (integer) - Even Strength Goals.
  - **`evsg_per_game`** (number, decimal) - Even strength goals per game (evsg/games_played).
  - **`ppgl`** (integer) - Power Play Goals — goals scored with man advantage.
  - **`ppgl_per_game`** (number, decimal) - Power play goals per game. (ppgl/games_played).
  - **`shg`** (integer) - Short-handed Goals — goals scored when team is short-handed.
  - **`shg_per_game`** (number, decimal) - Short-handed goals per game. (shg/games_played).
  - **`gwg`** (integer) - Game-Winning Goals.
  - **`gwg_per_game`** (number, decimal) - Game-winning goals per game. (gwg/games_played).
  - **`evsa`** (integer) - Even Strength Assists — assists at even strength.
  - **`evsa_per_game`** (number, decimal) - Even strength assists per game. (evsa/games_played).
  - **`ppa`** (integer) - Power Play Assists — assists on power play goals.
  - **`ppa_per_game`** (number, decimal) - Power play assists per game. (ppa/games_played).
  - **`sha`** (integer) - Short-handed Assists — assists while team is short-handed.
  - **`sha_per_game`** (number, decimal) - Short-handed assists per game. (sha/games_played).
  - **`sog`** (integer) - Shots on Goal.
  - **`sog_per_game`** (number, decimal) - Shots on goal per game. (sog/games_played).
  - **`shp`** (number, decimal) - Shooting percentage, as a number (typically XX.X). No percent sign.
  - **`shp_decimal`** (number, decimal) - Shooting percentage, as a decimal fraction (e.g., 12.6% → 0.126).
  - **`toi`** (string) - Total time on ice for the season — expressed as mm:ss.
  - **`toi_decimal`** (number, decimal) - Total time on ice, as decimal minutes.
  - **`atoi`** (string) - Average time on ice per game (mm:ss).
  - **`atoi_decimal`** (number, decimal) - Average time on ice per game, decimal minutes.
  - **`tsa`** (integer) - Total Shot Attempts (2007–08 and later season).
  - **`tsa_per_game`** (number, decimal) - Total Shot Attempts per game. (tsa/games_played) (2007–08 and later season).
  - **`fow`** (integer) - Faceoff Wins (2007–08 and later season).
  - **`fow_per_game`** (number, decimal) - Faceoff Wins per game. (fow/games_played) (2007–08 and later season).
  - **`fol`** (integer) - Faceoff Losses (2007–08 and later season).
  - **`fol_per_game`** (number, decimal) - Faceoff Losses per game. (fol/games_played) (2007–08 and later season).
  - **`fo_per`** (number, decimal) - Faceoff Win Percentage, as percent (e.g., 52.1). (2007–08 and later season).
  - **`fol_per_decimal`** (number, decimal) - Faceoff win rate, decimal (e.g., 0.521). (2007–08 and later season).
  - **`blk`** (integer) - Blocked Shots: number of opponent shots blocked. (2007–08 and later season).
  - **`blk_per_game`** (number, decimal) - Blocked shots per game. (blk/games_played) (2007–08 and later season).
  - **`hit`** (integer) - Hits. (2007–08 and later season).
  - **`hit_per_game`** (number, decimal) - Hits per game. (hit/games_played) (2007–08 and later season).
  - **`take`** (integer) - Takeaways. (2007–08 and later season).
  - **`tak_per_game`** (number, decimal) - Takeaways per game. (take/games_played) (2007–08 and later season).
  - **`give`** (integer) - Giveaways. (2007–08 and later season).
  - **`give_per_game`** (number, decimal) - Giveaways per game. (give/games_played) (2007–08 and later season).
  - **`awards`** (string) - List of any individual awards received.

  > [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played.**
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_regular_season_20212022/position/RW/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_regular_season_now/position/RW/
```
<a name="basic_stats_players_playoff_{year}"></a>
### 2.17 Get basic stats players playoff by year
- **Endpoint:** `/basic_stats_players_playoff_{year}/`
- **Method:** GET
- **Description:** Returns a table of basic individual player statistics for the specified NHL playoff. Each object represents a player’s statistical profile for that season. For seasons from 2007–08 onward, contains additional columns such as total shot attempts and faceoff stats..
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`goals`** (integer) - Goals scored.
  - **`goals_per_game`** (number, decimal) - Goals per game (goals/games_played).
  - **`assists`** (integer) - Assists.
  - **`assists_per_game`** (number, decimal) - Assists per game (assists/games_played).
  - **`points`** (integer) - Points (Goals + Assists).
  - **`points_per_game`** (number, decimal) - Points per game (points/games_played).
  - **`xpm`** (integer) - Plus/Minus Rating (net difference in goals scored and allowed on the ice with this player's participation).
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game (xpm/games_played).
  - **`pim`** (integer) - Penalties in Minutes — total penalty minutes accrued.
  - **`pim_per_game`** (number, decimal) - Penalty minutes per game. (pim/games_played).
  - **`evsg`** (integer) - Even Strength Goals.
  - **`evsg_per_game`** (number, decimal) - Even strength goals per game (evsg/games_played).
  - **`ppgl`** (integer) - Power Play Goals — goals scored with man advantage.
  - **`ppgl_per_game`** (number, decimal) - Power play goals per game. (ppgl/games_played).
  - **`shg`** (integer) - Short-handed Goals — goals scored when team is short-handed.
  - **`shg_per_game`** (number, decimal) - Short-handed goals per game. (shg/games_played).
  - **`gwg`** (integer) - Game-Winning Goals.
  - **`gwg_per_game`** (number, decimal) - Game-winning goals per game. (gwg/games_played).
  - **`evsa`** (integer) - Even Strength Assists — assists at even strength.
  - **`evsa_per_game`** (number, decimal) - Even strength assists per game. (evsa/games_played).
  - **`ppa`** (integer) - Power Play Assists — assists on power play goals.
  - **`ppa_per_game`** (number, decimal) - Power play assists per game. (ppa/games_played).
  - **`sha`** (integer) - Short-handed Assists — assists while team is short-handed.
  - **`sha_per_game`** (number, decimal) - Short-handed assists per game. (sha/games_played).
  - **`sog`** (integer) - Shots on Goal.
  - **`sog_per_game`** (number, decimal) - Shots on goal per game. (sog/games_played).
  - **`shp`** (number, decimal) - Shooting percentage, as a number (typically XX.X). No percent sign.
  - **`shp_decimal`** (number, decimal) - Shooting percentage, as a decimal fraction (e.g., 12.6% → 0.126).
  - **`toi`** (string) - Total time on ice for the season — expressed as mm:ss.
  - **`toi_decimal`** (number, decimal) - Total time on ice, as decimal minutes.
  - **`atoi`** (string) - Average time on ice per game (mm:ss).
  - **`atoi_decimal`** (number, decimal) - Average time on ice per game, decimal minutes.
  - **`tsa`** (integer) - Total Shot Attempts (2007–08 and later season).
  - **`tsa_per_game`** (number, decimal) - Total Shot Attempts per game. (tsa/games_played) (2007–08 and later season).
  - **`fow`** (integer) - Faceoff Wins (2007–08 and later season).
  - **`fow_per_game`** (number, decimal) - Faceoff Wins per game. (fow/games_played) (2007–08 and later season).
  - **`fol`** (integer) - Faceoff Losses (2007–08 and later season).
  - **`fol_per_game`** (number, decimal) - Faceoff Losses per game. (fol/games_played) (2007–08 and later season).
  - **`fo_per`** (number, decimal) - Faceoff Win Percentage, as percent (e.g., 52.1). (2007–08 and later season).
  - **`fol_per_decimal`** (number, decimal) - Faceoff win rate, decimal (e.g., 0.521). (2007–08 and later season).
  - **`blk`** (integer) - Blocked Shots: number of opponent shots blocked. (2007–08 and later season).
  - **`blk_per_game`** (number, decimal) - Blocked shots per game. (blk/games_played) (2007–08 and later season).
  - **`hit`** (integer) - Hits. (2007–08 and later season).
  - **`hit_per_game`** (number, decimal) - Hits per game. (hit/games_played) (2007–08 and later season).
  - **`take`** (integer) - Takeaways. (2007–08 and later season).
  - **`tak_per_game`** (number, decimal) - Takeaways per game. (take/games_played) (2007–08 and later season).
  - **`give`** (integer) - Giveaways. (2007–08 and later season).
  - **`give_per_game`** (number, decimal) - Giveaways per game. (give/games_played) (2007–08 and later season).
  - **`awards`** (string) - List of any individual awards received.
    
> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played.**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_playoff_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_playoff_now/
```
<a name="basic_stats_players_playoff_{year}/rank/{rank}"></a>
### 2.18 Get basic stats players playoff by year and specific rank
- **Endpoint:** `/basic_stats_players_playoff_{year}/rank/{rank}/`
- **Method:** GET
- **Description:** Returns a table of basic individual player statistics for the specified NHL playoff by rank. Each object represents a player’s statistical profile for that season. For seasons from 2007–08 onward, contains additional columns such as total shot attempts and faceoff stats.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`goals`** (integer) - Goals scored.
  - **`goals_per_game`** (number, decimal) - Goals per game (goals/games_played).
  - **`assists`** (integer) - Assists.
  - **`assists_per_game`** (number, decimal) - Assists per game (assists/games_played).
  - **`points`** (integer) - Points (Goals + Assists).
  - **`points_per_game`** (number, decimal) - Points per game (points/games_played).
  - **`xpm`** (integer) - Plus/Minus Rating (net difference in goals scored and allowed on the ice with this player's participation).
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game (xpm/games_played).
  - **`pim`** (integer) - Penalties in Minutes — total penalty minutes accrued.
  - **`pim_per_game`** (number, decimal) - Penalty minutes per game. (pim/games_played).
  - **`evsg`** (integer) - Even Strength Goals.
  - **`evsg_per_game`** (number, decimal) - Even strength goals per game (evsg/games_played).
  - **`ppgl`** (integer) - Power Play Goals — goals scored with man advantage.
  - **`ppgl_per_game`** (number, decimal) - Power play goals per game. (ppgl/games_played).
  - **`shg`** (integer) - Short-handed Goals — goals scored when team is short-handed.
  - **`shg_per_game`** (number, decimal) - Short-handed goals per game. (shg/games_played).
  - **`gwg`** (integer) - Game-Winning Goals.
  - **`gwg_per_game`** (number, decimal) - Game-winning goals per game. (gwg/games_played).
  - **`evsa`** (integer) - Even Strength Assists — assists at even strength.
  - **`evsa_per_game`** (number, decimal) - Even strength assists per game. (evsa/games_played).
  - **`ppa`** (integer) - Power Play Assists — assists on power play goals.
  - **`ppa_per_game`** (number, decimal) - Power play assists per game. (ppa/games_played).
  - **`sha`** (integer) - Short-handed Assists — assists while team is short-handed.
  - **`sha_per_game`** (number, decimal) - Short-handed assists per game. (sha/games_played).
  - **`sog`** (integer) - Shots on Goal.
  - **`sog_per_game`** (number, decimal) - Shots on goal per game. (sog/games_played).
  - **`shp`** (number, decimal) - Shooting percentage, as a number (typically XX.X). No percent sign.
  - **`shp_decimal`** (number, decimal) - Shooting percentage, as a decimal fraction (e.g., 12.6% → 0.126).
  - **`toi`** (string) - Total time on ice for the season — expressed as mm:ss.
  - **`toi_decimal`** (number, decimal) - Total time on ice, as decimal minutes.
  - **`atoi`** (string) - Average time on ice per game (mm:ss).
  - **`atoi_decimal`** (number, decimal) - Average time on ice per game, decimal minutes.
  - **`tsa`** (integer) - Total Shot Attempts (2007–08 and later season).
  - **`tsa_per_game`** (number, decimal) - Total Shot Attempts per game. (tsa/games_played) (2007–08 and later season).
  - **`fow`** (integer) - Faceoff Wins (2007–08 and later season).
  - **`fow_per_game`** (number, decimal) - Faceoff Wins per game. (fow/games_played) (2007–08 and later season).
  - **`fol`** (integer) - Faceoff Losses (2007–08 and later season).
  - **`fol_per_game`** (number, decimal) - Faceoff Losses per game. (fol/games_played) (2007–08 and later season).
  - **`fo_per`** (number, decimal) - Faceoff Win Percentage, as percent (e.g., 52.1). (2007–08 and later season).
  - **`fol_per_decimal`** (number, decimal) - Faceoff win rate, decimal (e.g., 0.521). (2007–08 and later season).
  - **`blk`** (integer) - Blocked Shots: number of opponent shots blocked. (2007–08 and later season).
  - **`blk_per_game`** (number, decimal) - Blocked shots per game. (blk/games_played) (2007–08 and later season).
  - **`hit`** (integer) - Hits. (2007–08 and later season).
  - **`hit_per_game`** (number, decimal) - Hits per game. (hit/games_played) (2007–08 and later season).
  - **`take`** (integer) - Takeaways. (2007–08 and later season).
  - **`tak_per_game`** (number, decimal) - Takeaways per game. (take/games_played) (2007–08 and later season).
  - **`give`** (integer) - Giveaways. (2007–08 and later season).
  - **`give_per_game`** (number, decimal) - Giveaways per game. (give/games_played) (2007–08 and later season).
  - **`awards`** (string) - List of any individual awards received.

> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played.**
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_playoff_20212022/rank/17
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_playoff_now/rank/17
```
<a name="basic_stats_players_playoff_{year}/team_abbrev/{team_abbrev}"></a>
### 2.19 Get basic stats players playoff by year and specific team
- **Endpoint:** `/basic_stats_players_playoff_{year}/team_abbrev/{team_abbrev}/`
- **Method:** GET
- **Description:** Returns a table of basic individual player statistics for the specified NHL playoff by team. Each object represents a player’s statistical profile for that season. For seasons from 2007–08 onward, contains additional columns such as total shot attempts and faceoff stats.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`goals`** (integer) - Goals scored.
  - **`goals_per_game`** (number, decimal) - Goals per game (goals/games_played).
  - **`assists`** (integer) - Assists.
  - **`assists_per_game`** (number, decimal) - Assists per game (assists/games_played).
  - **`points`** (integer) - Points (Goals + Assists).
  - **`points_per_game`** (number, decimal) - Points per game (points/games_played).
  - **`xpm`** (integer) - Plus/Minus Rating (net difference in goals scored and allowed on the ice with this player's participation).
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game (xpm/games_played).
  - **`pim`** (integer) - Penalties in Minutes — total penalty minutes accrued.
  - **`pim_per_game`** (number, decimal) - Penalty minutes per game. (pim/games_played).
  - **`evsg`** (integer) - Even Strength Goals.
  - **`evsg_per_game`** (number, decimal) - Even strength goals per game (evsg/games_played).
  - **`ppgl`** (integer) - Power Play Goals — goals scored with man advantage.
  - **`ppgl_per_game`** (number, decimal) - Power play goals per game. (ppgl/games_played).
  - **`shg`** (integer) - Short-handed Goals — goals scored when team is short-handed.
  - **`shg_per_game`** (number, decimal) - Short-handed goals per game. (shg/games_played).
  - **`gwg`** (integer) - Game-Winning Goals.
  - **`gwg_per_game`** (number, decimal) - Game-winning goals per game. (gwg/games_played).
  - **`evsa`** (integer) - Even Strength Assists — assists at even strength.
  - **`evsa_per_game`** (number, decimal) - Even strength assists per game. (evsa/games_played).
  - **`ppa`** (integer) - Power Play Assists — assists on power play goals.
  - **`ppa_per_game`** (number, decimal) - Power play assists per game. (ppa/games_played).
  - **`sha`** (integer) - Short-handed Assists — assists while team is short-handed.
  - **`sha_per_game`** (number, decimal) - Short-handed assists per game. (sha/games_played).
  - **`sog`** (integer) - Shots on Goal.
  - **`sog_per_game`** (number, decimal) - Shots on goal per game. (sog/games_played).
  - **`shp`** (number, decimal) - Shooting percentage, as a number (typically XX.X). No percent sign.
  - **`shp_decimal`** (number, decimal) - Shooting percentage, as a decimal fraction (e.g., 12.6% → 0.126).
  - **`toi`** (string) - Total time on ice for the season — expressed as mm:ss.
  - **`toi_decimal`** (number, decimal) - Total time on ice, as decimal minutes.
  - **`atoi`** (string) - Average time on ice per game (mm:ss).
  - **`atoi_decimal`** (number, decimal) - Average time on ice per game, decimal minutes.
  - **`tsa`** (integer) - Total Shot Attempts (2007–08 and later season).
  - **`tsa_per_game`** (number, decimal) - Total Shot Attempts per game. (tsa/games_played) (2007–08 and later season).
  - **`fow`** (integer) - Faceoff Wins (2007–08 and later season).
  - **`fow_per_game`** (number, decimal) - Faceoff Wins per game. (fow/games_played) (2007–08 and later season).
  - **`fol`** (integer) - Faceoff Losses (2007–08 and later season).
  - **`fol_per_game`** (number, decimal) - Faceoff Losses per game. (fol/games_played) (2007–08 and later season).
  - **`fo_per`** (number, decimal) - Faceoff Win Percentage, as percent (e.g., 52.1). (2007–08 and later season).
  - **`fol_per_decimal`** (number, decimal) - Faceoff win rate, decimal (e.g., 0.521). (2007–08 and later season).
  - **`blk`** (integer) - Blocked Shots: number of opponent shots blocked. (2007–08 and later season).
  - **`blk_per_game`** (number, decimal) - Blocked shots per game. (blk/games_played) (2007–08 and later season).
  - **`hit`** (integer) - Hits. (2007–08 and later season).
  - **`hit_per_game`** (number, decimal) - Hits per game. (hit/games_played) (2007–08 and later season).
  - **`take`** (integer) - Takeaways. (2007–08 and later season).
  - **`tak_per_game`** (number, decimal) - Takeaways per game. (take/games_played) (2007–08 and later season).
  - **`give`** (integer) - Giveaways. (2007–08 and later season).
  - **`give_per_game`** (number, decimal) - Giveaways per game. (give/games_played) (2007–08 and later season).
  - **`awards`** (string) - List of any individual awards received.

> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played.**
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_playoff_20212022/team_abbrev/BOS/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_playoff_now/team_abbrev/BOS/
```
<a name="basic_stats_players_playoff_{year}/player_id/{player_id}"></a>
### 2.20 Get basic stats players playoff by year and player ID
- **Endpoint:** `/basic_stats_players_playoff_{year}/player_id/{player_id}/`
- **Method:** GET
- **Description:** Returns a table of basic individual player statistics for the specified NHL playoff by player ID. Each object represents a player’s statistical profile for that season. For seasons from 2007–08 onward, contains additional columns such as total shot attempts and faceoff stats.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`goals`** (integer) - Goals scored.
  - **`goals_per_game`** (number, decimal) - Goals per game (goals/games_played).
  - **`assists`** (integer) - Assists.
  - **`assists_per_game`** (number, decimal) - Assists per game (assists/games_played).
  - **`points`** (integer) - Points (Goals + Assists).
  - **`points_per_game`** (number, decimal) - Points per game (points/games_played).
  - **`xpm`** (integer) - Plus/Minus Rating (net difference in goals scored and allowed on the ice with this player's participation).
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game (xpm/games_played).
  - **`pim`** (integer) - Penalties in Minutes — total penalty minutes accrued.
  - **`pim_per_game`** (number, decimal) - Penalty minutes per game. (pim/games_played).
  - **`evsg`** (integer) - Even Strength Goals.
  - **`evsg_per_game`** (number, decimal) - Even strength goals per game (evsg/games_played).
  - **`ppgl`** (integer) - Power Play Goals — goals scored with man advantage.
  - **`ppgl_per_game`** (number, decimal) - Power play goals per game. (ppgl/games_played).
  - **`shg`** (integer) - Short-handed Goals — goals scored when team is short-handed.
  - **`shg_per_game`** (number, decimal) - Short-handed goals per game. (shg/games_played).
  - **`gwg`** (integer) - Game-Winning Goals.
  - **`gwg_per_game`** (number, decimal) - Game-winning goals per game. (gwg/games_played).
  - **`evsa`** (integer) - Even Strength Assists — assists at even strength.
  - **`evsa_per_game`** (number, decimal) - Even strength assists per game. (evsa/games_played).
  - **`ppa`** (integer) - Power Play Assists — assists on power play goals.
  - **`ppa_per_game`** (number, decimal) - Power play assists per game. (ppa/games_played).
  - **`sha`** (integer) - Short-handed Assists — assists while team is short-handed.
  - **`sha_per_game`** (number, decimal) - Short-handed assists per game. (sha/games_played).
  - **`sog`** (integer) - Shots on Goal.
  - **`sog_per_game`** (number, decimal) - Shots on goal per game. (sog/games_played).
  - **`shp`** (number, decimal) - Shooting percentage, as a number (typically XX.X). No percent sign.
  - **`shp_decimal`** (number, decimal) - Shooting percentage, as a decimal fraction (e.g., 12.6% → 0.126).
  - **`toi`** (string) - Total time on ice for the season — expressed as mm:ss.
  - **`toi_decimal`** (number, decimal) - Total time on ice, as decimal minutes.
  - **`atoi`** (string) - Average time on ice per game (mm:ss).
  - **`atoi_decimal`** (number, decimal) - Average time on ice per game, decimal minutes.
  - **`tsa`** (integer) - Total Shot Attempts (2007–08 and later season).
  - **`tsa_per_game`** (number, decimal) - Total Shot Attempts per game. (tsa/games_played) (2007–08 and later season).
  - **`fow`** (integer) - Faceoff Wins (2007–08 and later season).
  - **`fow_per_game`** (number, decimal) - Faceoff Wins per game. (fow/games_played) (2007–08 and later season).
  - **`fol`** (integer) - Faceoff Losses (2007–08 and later season).
  - **`fol_per_game`** (number, decimal) - Faceoff Losses per game. (fol/games_played) (2007–08 and later season).
  - **`fo_per`** (number, decimal) - Faceoff Win Percentage, as percent (e.g., 52.1). (2007–08 and later season).
  - **`fol_per_decimal`** (number, decimal) - Faceoff win rate, decimal (e.g., 0.521). (2007–08 and later season).
  - **`blk`** (integer) - Blocked Shots: number of opponent shots blocked. (2007–08 and later season).
  - **`blk_per_game`** (number, decimal) - Blocked shots per game. (blk/games_played) (2007–08 and later season).
  - **`hit`** (integer) - Hits. (2007–08 and later season).
  - **`hit_per_game`** (number, decimal) - Hits per game. (hit/games_played) (2007–08 and later season).
  - **`take`** (integer) - Takeaways. (2007–08 and later season).
  - **`tak_per_game`** (number, decimal) - Takeaways per game. (take/games_played) (2007–08 and later season).
  - **`give`** (integer) - Giveaways. (2007–08 and later season).
  - **`give_per_game`** (number, decimal) - Giveaways per game. (give/games_played) (2007–08 and later season).
  - **`awards`** (string) - List of any individual awards received.

> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played.**
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_playoff_20212022/player_id/ahose01/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_playoff_now/player_id/ahose01/
```
<a name="basic_stats_players_playoff_{year}/position/{position}"></a>
### 2.21 Get basic stats players playoff by year and position
- **Endpoint:** `/basic_stats_players_playoff_{year}/position/{position}/`
- **Method:** GET
- **Description:** Returns a table of basic individual player statistics for the specified NHL playoff by position player. Each object represents a player’s statistical profile for that season. For seasons from 2007–08 onward, contains additional columns such as total shot attempts and faceoff stats.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`position`** (string) - Primary position played (C, LW, RW, D).
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`goals`** (integer) - Goals scored.
  - **`goals_per_game`** (number, decimal) - Goals per game (goals/games_played).
  - **`assists`** (integer) - Assists.
  - **`assists_per_game`** (number, decimal) - Assists per game (assists/games_played).
  - **`points`** (integer) - Points (Goals + Assists).
  - **`points_per_game`** (number, decimal) - Points per game (points/games_played).
  - **`xpm`** (integer) - Plus/Minus Rating (net difference in goals scored and allowed on the ice with this player's participation).
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game (xpm/games_played).
  - **`pim`** (integer) - Penalties in Minutes — total penalty minutes accrued.
  - **`pim_per_game`** (number, decimal) - Penalty minutes per game. (pim/games_played).
  - **`evsg`** (integer) - Even Strength Goals.
  - **`evsg_per_game`** (number, decimal) - Even strength goals per game (evsg/games_played).
  - **`ppgl`** (integer) - Power Play Goals — goals scored with man advantage.
  - **`ppgl_per_game`** (number, decimal) - Power play goals per game. (ppgl/games_played).
  - **`shg`** (integer) - Short-handed Goals — goals scored when team is short-handed.
  - **`shg_per_game`** (number, decimal) - Short-handed goals per game. (shg/games_played).
  - **`gwg`** (integer) - Game-Winning Goals.
  - **`gwg_per_game`** (number, decimal) - Game-winning goals per game. (gwg/games_played).
  - **`evsa`** (integer) - Even Strength Assists — assists at even strength.
  - **`evsa_per_game`** (number, decimal) - Even strength assists per game. (evsa/games_played).
  - **`ppa`** (integer) - Power Play Assists — assists on power play goals.
  - **`ppa_per_game`** (number, decimal) - Power play assists per game. (ppa/games_played).
  - **`sha`** (integer) - Short-handed Assists — assists while team is short-handed.
  - **`sha_per_game`** (number, decimal) - Short-handed assists per game. (sha/games_played).
  - **`sog`** (integer) - Shots on Goal.
  - **`sog_per_game`** (number, decimal) - Shots on goal per game. (sog/games_played).
  - **`shp`** (number, decimal) - Shooting percentage, as a number (typically XX.X). No percent sign.
  - **`shp_decimal`** (number, decimal) - Shooting percentage, as a decimal fraction (e.g., 12.6% → 0.126).
  - **`toi`** (string) - Total time on ice for the season — expressed as mm:ss.
  - **`toi_decimal`** (number, decimal) - Total time on ice, as decimal minutes.
  - **`atoi`** (string) - Average time on ice per game (mm:ss).
  - **`atoi_decimal`** (number, decimal) - Average time on ice per game, decimal minutes.
  - **`tsa`** (integer) - Total Shot Attempts (2007–08 and later season).
  - **`tsa_per_game`** (number, decimal) - Total Shot Attempts per game. (tsa/games_played) (2007–08 and later season).
  - **`fow`** (integer) - Faceoff Wins (2007–08 and later season).
  - **`fow_per_game`** (number, decimal) - Faceoff Wins per game. (fow/games_played) (2007–08 and later season).
  - **`fol`** (integer) - Faceoff Losses (2007–08 and later season).
  - **`fol_per_game`** (number, decimal) - Faceoff Losses per game. (fol/games_played) (2007–08 and later season).
  - **`fo_per`** (number, decimal) - Faceoff Win Percentage, as percent (e.g., 52.1). (2007–08 and later season).
  - **`fol_per_decimal`** (number, decimal) - Faceoff win rate, decimal (e.g., 0.521). (2007–08 and later season).
  - **`blk`** (integer) - Blocked Shots: number of opponent shots blocked. (2007–08 and later season).
  - **`blk_per_game`** (number, decimal) - Blocked shots per game. (blk/games_played) (2007–08 and later season).
  - **`hit`** (integer) - Hits. (2007–08 and later season).
  - **`hit_per_game`** (number, decimal) - Hits per game. (hit/games_played) (2007–08 and later season).
  - **`take`** (integer) - Takeaways. (2007–08 and later season).
  - **`tak_per_game`** (number, decimal) - Takeaways per game. (take/games_played) (2007–08 and later season).
  - **`give`** (integer) - Giveaways. (2007–08 and later season).
  - **`give_per_game`** (number, decimal) - Giveaways per game. (give/games_played) (2007–08 and later season).
  - **`awards`** (string) - List of any individual awards received.

> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played.**
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_playoff_20212022/position/RW/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/basic_stats_players_playoff_now/position/RW/
```
<a name="miscellaneous_stats_players_regular_season_{year}"></a>
### 2.22 Get miscellaneous stats players regular season by year
- **Endpoint:** `/miscellaneous_stats_players_regular_season_{year}/`
- **Method:** GET
- **Description:** Returns a table of miscellaneous individual NHL player statistics for the specified regular season. Each object represents a player's advanced and miscellaneous stats profile for that season, such as adjusted goals, expected plus-minus, point shares, shootout data, and more. 
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`goals_adjusted`** (integer) - Adjusted Goals - adjusted stats are normalized to an 82-game schedule, 18 skaters and league averages of 6 goals/game and 1.67 assists/goal.
  - **`goals_adjusted_per_game`** (number, decimal) -  Adjusted Goals per game.
  - **`assists_adjusted`** (integer) -Adjusted Assists - adjusted stats are normalized to an 82-game schedule, 18 skaters and league averages of 6 goals/game and 1.67 assists/goal.
  - **`assists_adjusted_per_game`** (number, decimal) - Adjusted Assists per game.
  - **`points_adjusted`** (integer) - Adjusted Points.
  - **`points_adjusted_per_game`** (number, decimal) -  Adjusted Points per game.
  - **`goals_created_adjusted`** (number, decimal) - Adjusted Goals Created.
  - **`goals_created_adjusted_per_game`** (number, decimal) - Adjusted Goals Created per game.
  - **`total_goals_for`** (integer) - Total Goals On-Ice For.
  - **`total_goals_for_per_game`** (number, decimal) - Total Goals On-Ice For per game. 
  - **`power_play_goals_for`** (integer) - Power play goals for while the player was on the ice.
  - **`power_play_goals_for_per_game`** (number, decimal) - Power play goals per game.
  - **`total_goals_against`** (integer) - Total Goals On-Ice Against.
  - **`total_goals_against_per_game`** (number, decimal) -  Total Goals On-Ice Against per game.
  - **`power_play_goals_against`** (integer) - Power play goals against while the player was on the ice.
  - **`power_play_goals_against_per_game`** (number, decimal) - Power play goals against per game. 
  - **`xpm`** (integer) - Plus/Minus.
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game. 
  - **`ops`** (number, decimal) - Offensive Point Shares - an estimate of the number of points contributed by a player due to his offense.
  - **`ops_per_game`** (number, decimal) - Offensive Point Shares per game.
  - **`ops_decimal`** (number, decimal) - Offensive Point Shares (Exact value without rounding the number).
  - **`ops_decimal_per_game`** (number, decimal) - Offensive Point Shares (Exact value without rounding the number) per game. 
  - **`dps`** (number, decimal) - Defensive Point Shares - an estimate of the number of points contributed by a player due to his defense.
  - **`dps_per_game`** (number, decimal) - Defensive Point Shares per game. 
  - **`dps_decimal`** (number, decimal) - Defensive Point Shares (Exact value without rounding the number).
  - **`dps_decimal_per_game`** (number, decimal) -  Defensive Point Shares (Exact value without rounding the number) per game. 
  - **`ps`** (number, decimal) - Point Shares - an estimate of the number of points contributed by a player.
  - **`ps_per_game`** (number, decimal) - Point Shares per game. 
  - **`ps_decimal`** (number, decimal) - Point Shares (Exact value without rounding the number).
  - **`ps_decimal_per_game`** (number, decimal) - Point Shares (Exact value without rounding the number) per game.
  - **`shootouts_att`** (integer) - Shootout attempts. (2007–08 and later season)
  - **`shootouts_att_per_game`** (number, decimal) - Shootout attempts per game. (2007–08 and later season)
  - **`shootouts_made`** (integer) - Shootout shots made. (2007–08 and later season)
  - **`shootouts_made_per_game`** (number, decimal) - Shootout shots made per game. (2007–08 and later season)
  - **`shootouts_miss`** (integer) - Shootout shots missed. (2007–08 and later season)
  - **`shootouts_miss_per_game`** (number, decimal) - Shootout shots missed per game. (2007–08 and later season)
  - **`shootouts_made_pct`** (number, decimal) - Percentage of shootout attempts converted. (2007–08 and later season)
  - **`shootouts_made_pct_per_game`** (number, decimal) - Percentage of shootout attempts converted per game. (2007–08 and later season)
  - **`shootouts_made_pct_decimal`** (number, decimal) - Percentage of shootout attempts converted as a decimal (e.g., 0.370). (2007–08 and later season)
  - **`shootouts_made_pct_decimal_per_game`** (number, decimal) - Percentage of shootout attempts converted as a decimal per game. (2007–08 and later season)
  - **`ev_exp_on_goals_for`** (number, decimal) - 'Expected Goals For' given where shots came from, for and against, while this player was on the ice at even strength. It's based on where the shots are coming from, compared to the league-wide shooting percentage for that shot location. (2014–15 and later season)
  - **`ev_exp_on_goals_for_per_game`** (number, decimal) - Expected Goals For per game. (2014–15 and later season)
  - **`ev_exp_on_goals_against`** (number, decimal) - 'Expected Goals Against' given where shots came from, for and against, while this player was on the ice at even strength. It's based on where the shots are coming from, compared to the league-wide shooting percentage for that shot location. (2014–15 and later season)
  - **`ev_exp_on_goals_against_per_game`** (number, decimal) - Expected Goals Against per game. (2014–15 and later season)
  - **`expected_plsmns`** (number, decimal) - 'Expected +/-' given where shots came from, for and against, while this player was on the ice at even strength. It's based on where the shots are coming from, compared to the league-wide shooting percentage for that shot location. (2014–15 and later season)
  - **`expected_plsmns_per_game`** (number, decimal) - Expected +/- per game. (2014–15 and later season)
  - **`awards`** (string) - List of any individual awards received.

> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played.**
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_regular_season_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_regular_season_now/
```
<a name="miscellaneous_stats_players_regular_season_{year}/rank/{rank}"></a>
### 2.23 Get miscellaneous stats players regular season by year and specific rank
- **Endpoint:** `/miscellaneous_stats_players_regular_season_{year}/rank/{rank}/`
- **Method:** GET
- **Description:** Returns a table of miscellaneous individual NHL player statistics for the specified regular season by specific rank. Each object represents a player's advanced and miscellaneous stats profile for that season, such as adjusted goals, expected plus-minus, point shares, shootout data, and more. 
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{rank}`** (integer) - Rank in the leaderboard, first place is the best.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`goals_adjusted`** (integer) - Adjusted Goals - adjusted stats are normalized to an 82-game schedule, 18 skaters and league averages of 6 goals/game and 1.67 assists/goal.
  - **`goals_adjusted_per_game`** (number, decimal) -  Adjusted Goals per game.
  - **`assists_adjusted`** (integer) -Adjusted Assists - adjusted stats are normalized to an 82-game schedule, 18 skaters and league averages of 6 goals/game and 1.67 assists/goal.
  - **`assists_adjusted_per_game`** (number, decimal) - Adjusted Assists per game.
  - **`points_adjusted`** (integer) - Adjusted Points.
  - **`points_adjusted_per_game`** (number, decimal) -  Adjusted Points per game.
  - **`goals_created_adjusted`** (number, decimal) - Adjusted Goals Created.
  - **`goals_created_adjusted_per_game`** (number, decimal) - Adjusted Goals Created per game.
  - **`total_goals_for`** (integer) - Total Goals On-Ice For.
  - **`total_goals_for_per_game`** (number, decimal) - Total Goals On-Ice For per game. 
  - **`power_play_goals_for`** (integer) - Power play goals for while the player was on the ice.
  - **`power_play_goals_for_per_game`** (number, decimal) - Power play goals per game.
  - **`total_goals_against`** (integer) - Total Goals On-Ice Against.
  - **`total_goals_against_per_game`** (number, decimal) -  Total Goals On-Ice Against per game.
  - **`power_play_goals_against`** (integer) - Power play goals against while the player was on the ice.
  - **`power_play_goals_against_per_game`** (number, decimal) - Power play goals against per game. 
  - **`xpm`** (integer) - Plus/Minus.
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game. 
  - **`ops`** (number, decimal) - Offensive Point Shares - an estimate of the number of points contributed by a player due to his offense.
  - **`ops_per_game`** (number, decimal) - Offensive Point Shares per game.
  - **`ops_decimal`** (number, decimal) - Offensive Point Shares (Exact value without rounding the number).
  - **`ops_decimal_per_game`** (number, decimal) - Offensive Point Shares (Exact value without rounding the number) per game. 
  - **`dps`** (number, decimal) - Defensive Point Shares - an estimate of the number of points contributed by a player due to his defense.
  - **`dps_per_game`** (number, decimal) - Defensive Point Shares per game. 
  - **`dps_decimal`** (number, decimal) - Defensive Point Shares (Exact value without rounding the number).
  - **`dps_decimal_per_game`** (number, decimal) -  Defensive Point Shares (Exact value without rounding the number) per game. 
  - **`ps`** (number, decimal) - Point Shares - an estimate of the number of points contributed by a player.
  - **`ps_per_game`** (number, decimal) - Point Shares per game. 
  - **`ps_decimal`** (number, decimal) - Point Shares (Exact value without rounding the number).
  - **`ps_decimal_per_game`** (number, decimal) - Point Shares (Exact value without rounding the number) per game.
  - **`shootouts_att`** (integer) - Shootout attempts. (2007–08 and later season)
  - **`shootouts_att_per_game`** (number, decimal) - Shootout attempts per game. (2007–08 and later season)
  - **`shootouts_made`** (integer) - Shootout shots made. (2007–08 and later season)
  - **`shootouts_made_per_game`** (number, decimal) - Shootout shots made per game. (2007–08 and later season)
  - **`shootouts_miss`** (integer) - Shootout shots missed. (2007–08 and later season)
  - **`shootouts_miss_per_game`** (number, decimal) - Shootout shots missed per game. (2007–08 and later season)
  - **`shootouts_made_pct`** (number, decimal) - Percentage of shootout attempts converted. (2007–08 and later season)
  - **`shootouts_made_pct_per_game`** (number, decimal) - Percentage of shootout attempts converted per game. (2007–08 and later season)
  - **`shootouts_made_pct_decimal`** (number, decimal) - Percentage of shootout attempts converted as a decimal (e.g., 0.370). (2007–08 and later season)
  - **`shootouts_made_pct_decimal_per_game`** (number, decimal) - Percentage of shootout attempts converted as a decimal per game. (2007–08 and later season)
  - **`ev_exp_on_goals_for`** (number, decimal) - 'Expected Goals For' given where shots came from, for and against, while this player was on the ice at even strength. It's based on where the shots are coming from, compared to the league-wide shooting percentage for that shot location. (2014–15 and later season)
  - **`ev_exp_on_goals_for_per_game`** (number, decimal) - Expected Goals For per game. (2014–15 and later season)
  - **`ev_exp_on_goals_against`** (number, decimal) - 'Expected Goals Against' given where shots came from, for and against, while this player was on the ice at even strength. It's based on where the shots are coming from, compared to the league-wide shooting percentage for that shot location. (2014–15 and later season)
  - **`ev_exp_on_goals_against_per_game`** (number, decimal) - Expected Goals Against per game. (2014–15 and later season)
  - **`expected_plsmns`** (number, decimal) - 'Expected +/-' given where shots came from, for and against, while this player was on the ice at even strength. It's based on where the shots are coming from, compared to the league-wide shooting percentage for that shot location. (2014–15 and later season)
  - **`expected_plsmns_per_game`** (number, decimal) - Expected +/- per game. (2014–15 and later season)
  - **`awards`** (string) - List of any individual awards received.

> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played.**
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_regular_season_20212022/rank/12
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_regular_season_now/rank/12
```
<a name="miscellaneous_stats_players_regular_season_{year}/team_abbrev/{team_abbrev}"></a>
### 2.24 Get miscellaneous stats players regular season by year and specific team
- **Endpoint:** `/miscellaneous_stats_players_regular_season_{year}/team_abbrev/{team_abbrev}/`
- **Method:** GET
- **Description:** Returns a table of miscellaneous individual NHL player statistics for the specified regular season by specific team. Each object represents a player's advanced and miscellaneous stats profile for that season, such as adjusted goals, expected plus-minus, point shares, shootout data, and more. 
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{team_abbrev}`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`goals_adjusted`** (integer) - Adjusted Goals - adjusted stats are normalized to an 82-game schedule, 18 skaters and league averages of 6 goals/game and 1.67 assists/goal.
  - **`goals_adjusted_per_game`** (number, decimal) -  Adjusted Goals per game.
  - **`assists_adjusted`** (integer) -Adjusted Assists - adjusted stats are normalized to an 82-game schedule, 18 skaters and league averages of 6 goals/game and 1.67 assists/goal.
  - **`assists_adjusted_per_game`** (number, decimal) - Adjusted Assists per game.
  - **`points_adjusted`** (integer) - Adjusted Points.
  - **`points_adjusted_per_game`** (number, decimal) -  Adjusted Points per game.
  - **`goals_created_adjusted`** (number, decimal) - Adjusted Goals Created.
  - **`goals_created_adjusted_per_game`** (number, decimal) - Adjusted Goals Created per game.
  - **`total_goals_for`** (integer) - Total Goals On-Ice For.
  - **`total_goals_for_per_game`** (number, decimal) - Total Goals On-Ice For per game. 
  - **`power_play_goals_for`** (integer) - Power play goals for while the player was on the ice.
  - **`power_play_goals_for_per_game`** (number, decimal) - Power play goals per game.
  - **`total_goals_against`** (integer) - Total Goals On-Ice Against.
  - **`total_goals_against_per_game`** (number, decimal) -  Total Goals On-Ice Against per game.
  - **`power_play_goals_against`** (integer) - Power play goals against while the player was on the ice.
  - **`power_play_goals_against_per_game`** (number, decimal) - Power play goals against per game. 
  - **`xpm`** (integer) - Plus/Minus.
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game. 
  - **`ops`** (number, decimal) - Offensive Point Shares - an estimate of the number of points contributed by a player due to his offense.
  - **`ops_per_game`** (number, decimal) - Offensive Point Shares per game.
  - **`ops_decimal`** (number, decimal) - Offensive Point Shares (Exact value without rounding the number).
  - **`ops_decimal_per_game`** (number, decimal) - Offensive Point Shares (Exact value without rounding the number) per game. 
  - **`dps`** (number, decimal) - Defensive Point Shares - an estimate of the number of points contributed by a player due to his defense.
  - **`dps_per_game`** (number, decimal) - Defensive Point Shares per game. 
  - **`dps_decimal`** (number, decimal) - Defensive Point Shares (Exact value without rounding the number).
  - **`dps_decimal_per_game`** (number, decimal) -  Defensive Point Shares (Exact value without rounding the number) per game. 
  - **`ps`** (number, decimal) - Point Shares - an estimate of the number of points contributed by a player.
  - **`ps_per_game`** (number, decimal) - Point Shares per game. 
  - **`ps_decimal`** (number, decimal) - Point Shares (Exact value without rounding the number).
  - **`ps_decimal_per_game`** (number, decimal) - Point Shares (Exact value without rounding the number) per game.
  - **`shootouts_att`** (integer) - Shootout attempts. (2007–08 and later season)
  - **`shootouts_att_per_game`** (number, decimal) - Shootout attempts per game. (2007–08 and later season)
  - **`shootouts_made`** (integer) - Shootout shots made. (2007–08 and later season)
  - **`shootouts_made_per_game`** (number, decimal) - Shootout shots made per game. (2007–08 and later season)
  - **`shootouts_miss`** (integer) - Shootout shots missed. (2007–08 and later season)
  - **`shootouts_miss_per_game`** (number, decimal) - Shootout shots missed per game. (2007–08 and later season)
  - **`shootouts_made_pct`** (number, decimal) - Percentage of shootout attempts converted. (2007–08 and later season)
  - **`shootouts_made_pct_per_game`** (number, decimal) - Percentage of shootout attempts converted per game. (2007–08 and later season)
  - **`shootouts_made_pct_decimal`** (number, decimal) - Percentage of shootout attempts converted as a decimal (e.g., 0.370). (2007–08 and later season)
  - **`shootouts_made_pct_decimal_per_game`** (number, decimal) - Percentage of shootout attempts converted as a decimal per game. (2007–08 and later season)
  - **`ev_exp_on_goals_for`** (number, decimal) - 'Expected Goals For' given where shots came from, for and against, while this player was on the ice at even strength. It's based on where the shots are coming from, compared to the league-wide shooting percentage for that shot location. (2014–15 and later season)
  - **`ev_exp_on_goals_for_per_game`** (number, decimal) - Expected Goals For per game. (2014–15 and later season)
  - **`ev_exp_on_goals_against`** (number, decimal) - 'Expected Goals Against' given where shots came from, for and against, while this player was on the ice at even strength. It's based on where the shots are coming from, compared to the league-wide shooting percentage for that shot location. (2014–15 and later season)
  - **`ev_exp_on_goals_against_per_game`** (number, decimal) - Expected Goals Against per game. (2014–15 and later season)
  - **`expected_plsmns`** (number, decimal) - 'Expected +/-' given where shots came from, for and against, while this player was on the ice at even strength. It's based on where the shots are coming from, compared to the league-wide shooting percentage for that shot location. (2014–15 and later season)
  - **`expected_plsmns_per_game`** (number, decimal) - Expected +/- per game. (2014–15 and later season)
  - **`awards`** (string) - List of any individual awards received.

> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played.**
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_regular_season_20212022/team_abbrev/BOS/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_regular_season_now/team_abbrev/BOS/
```
<a name="miscellaneous_stats_players_regular_season_{year}/player_id/{player_id}"></a>
### 2.25 Get miscellaneous stats players regular season by year and player ID
- **Endpoint:** `/miscellaneous_stats_players_regular_season_{year}/player_id/{player_id}/`
- **Method:** GET
- **Description:** Returns a table of miscellaneous individual NHL player statistics for the specified regular season by player ID. Each object represents a player's advanced and miscellaneous stats profile for that season, such as adjusted goals, expected plus-minus, point shares, shootout data, and more. 
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{player_id}`** (string) - Unique identifier for each player, contains letters and numbers.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`goals_adjusted`** (integer) - Adjusted Goals - adjusted stats are normalized to an 82-game schedule, 18 skaters and league averages of 6 goals/game and 1.67 assists/goal.
  - **`goals_adjusted_per_game`** (number, decimal) -  Adjusted Goals per game.
  - **`assists_adjusted`** (integer) -Adjusted Assists - adjusted stats are normalized to an 82-game schedule, 18 skaters and league averages of 6 goals/game and 1.67 assists/goal.
  - **`assists_adjusted_per_game`** (number, decimal) - Adjusted Assists per game.
  - **`points_adjusted`** (integer) - Adjusted Points.
  - **`points_adjusted_per_game`** (number, decimal) -  Adjusted Points per game.
  - **`goals_created_adjusted`** (number, decimal) - Adjusted Goals Created.
  - **`goals_created_adjusted_per_game`** (number, decimal) - Adjusted Goals Created per game.
  - **`total_goals_for`** (integer) - Total Goals On-Ice For.
  - **`total_goals_for_per_game`** (number, decimal) - Total Goals On-Ice For per game. 
  - **`power_play_goals_for`** (integer) - Power play goals for while the player was on the ice.
  - **`power_play_goals_for_per_game`** (number, decimal) - Power play goals per game.
  - **`total_goals_against`** (integer) - Total Goals On-Ice Against.
  - **`total_goals_against_per_game`** (number, decimal) -  Total Goals On-Ice Against per game.
  - **`power_play_goals_against`** (integer) - Power play goals against while the player was on the ice.
  - **`power_play_goals_against_per_game`** (number, decimal) - Power play goals against per game. 
  - **`xpm`** (integer) - Plus/Minus.
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game. 
  - **`ops`** (number, decimal) - Offensive Point Shares - an estimate of the number of points contributed by a player due to his offense.
  - **`ops_per_game`** (number, decimal) - Offensive Point Shares per game.
  - **`ops_decimal`** (number, decimal) - Offensive Point Shares (Exact value without rounding the number).
  - **`ops_decimal_per_game`** (number, decimal) - Offensive Point Shares (Exact value without rounding the number) per game. 
  - **`dps`** (number, decimal) - Defensive Point Shares - an estimate of the number of points contributed by a player due to his defense.
  - **`dps_per_game`** (number, decimal) - Defensive Point Shares per game. 
  - **`dps_decimal`** (number, decimal) - Defensive Point Shares (Exact value without rounding the number).
  - **`dps_decimal_per_game`** (number, decimal) -  Defensive Point Shares (Exact value without rounding the number) per game. 
  - **`ps`** (number, decimal) - Point Shares - an estimate of the number of points contributed by a player.
  - **`ps_per_game`** (number, decimal) - Point Shares per game. 
  - **`ps_decimal`** (number, decimal) - Point Shares (Exact value without rounding the number).
  - **`ps_decimal_per_game`** (number, decimal) - Point Shares (Exact value without rounding the number) per game.
  - **`shootouts_att`** (integer) - Shootout attempts. (2007–08 and later season)
  - **`shootouts_att_per_game`** (number, decimal) - Shootout attempts per game. (2007–08 and later season)
  - **`shootouts_made`** (integer) - Shootout shots made. (2007–08 and later season)
  - **`shootouts_made_per_game`** (number, decimal) - Shootout shots made per game. (2007–08 and later season)
  - **`shootouts_miss`** (integer) - Shootout shots missed. (2007–08 and later season)
  - **`shootouts_miss_per_game`** (number, decimal) - Shootout shots missed per game. (2007–08 and later season)
  - **`shootouts_made_pct`** (number, decimal) - Percentage of shootout attempts converted. (2007–08 and later season)
  - **`shootouts_made_pct_per_game`** (number, decimal) - Percentage of shootout attempts converted per game. (2007–08 and later season)
  - **`shootouts_made_pct_decimal`** (number, decimal) - Percentage of shootout attempts converted as a decimal (e.g., 0.370). (2007–08 and later season)
  - **`shootouts_made_pct_decimal_per_game`** (number, decimal) - Percentage of shootout attempts converted as a decimal per game. (2007–08 and later season)
  - **`ev_exp_on_goals_for`** (number, decimal) - 'Expected Goals For' given where shots came from, for and against, while this player was on the ice at even strength. It's based on where the shots are coming from, compared to the league-wide shooting percentage for that shot location. (2014–15 and later season)
  - **`ev_exp_on_goals_for_per_game`** (number, decimal) - Expected Goals For per game. (2014–15 and later season)
  - **`ev_exp_on_goals_against`** (number, decimal) - 'Expected Goals Against' given where shots came from, for and against, while this player was on the ice at even strength. It's based on where the shots are coming from, compared to the league-wide shooting percentage for that shot location. (2014–15 and later season)
  - **`ev_exp_on_goals_against_per_game`** (number, decimal) - Expected Goals Against per game. (2014–15 and later season)
  - **`expected_plsmns`** (number, decimal) - 'Expected +/-' given where shots came from, for and against, while this player was on the ice at even strength. It's based on where the shots are coming from, compared to the league-wide shooting percentage for that shot location. (2014–15 and later season)
  - **`expected_plsmns_per_game`** (number, decimal) - Expected +/- per game. (2014–15 and later season)
  - **`awards`** (string) - List of any individual awards received.

> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played.**
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_regular_season_20212022/player_id/acciano01/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_regular_season_now/player_id/acciano01/
```
<a name="miscellaneous_stats_players_regular_season_{year}/position/{position}"></a>
### 2.26 Get miscellaneous stats players regular season by year and position
- **Endpoint:** `/miscellaneous_stats_players_regular_season_{year}/position/{position}/`
- **Method:** GET
- **Description:** Returns a table of miscellaneous individual NHL player statistics for the specified regular season by position. Each object represents a player's advanced and miscellaneous stats profile for that season, such as adjusted goals, expected plus-minus, point shares, shootout data, and more. 
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{position}`** (string) - Primary position played (C, LW, RW, D).
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`goals_adjusted`** (integer) - Adjusted Goals - adjusted stats are normalized to an 82-game schedule, 18 skaters and league averages of 6 goals/game and 1.67 assists/goal.
  - **`goals_adjusted_per_game`** (number, decimal) -  Adjusted Goals per game.
  - **`assists_adjusted`** (integer) -Adjusted Assists - adjusted stats are normalized to an 82-game schedule, 18 skaters and league averages of 6 goals/game and 1.67 assists/goal.
  - **`assists_adjusted_per_game`** (number, decimal) - Adjusted Assists per game.
  - **`points_adjusted`** (integer) - Adjusted Points.
  - **`points_adjusted_per_game`** (number, decimal) -  Adjusted Points per game.
  - **`goals_created_adjusted`** (number, decimal) - Adjusted Goals Created.
  - **`goals_created_adjusted_per_game`** (number, decimal) - Adjusted Goals Created per game.
  - **`total_goals_for`** (integer) - Total Goals On-Ice For.
  - **`total_goals_for_per_game`** (number, decimal) - Total Goals On-Ice For per game. 
  - **`power_play_goals_for`** (integer) - Power play goals for while the player was on the ice.
  - **`power_play_goals_for_per_game`** (number, decimal) - Power play goals per game.
  - **`total_goals_against`** (integer) - Total Goals On-Ice Against.
  - **`total_goals_against_per_game`** (number, decimal) -  Total Goals On-Ice Against per game.
  - **`power_play_goals_against`** (integer) - Power play goals against while the player was on the ice.
  - **`power_play_goals_against_per_game`** (number, decimal) - Power play goals against per game. 
  - **`xpm`** (integer) - Plus/Minus.
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game. 
  - **`ops`** (number, decimal) - Offensive Point Shares - an estimate of the number of points contributed by a player due to his offense.
  - **`ops_per_game`** (number, decimal) - Offensive Point Shares per game.
  - **`ops_decimal`** (number, decimal) - Offensive Point Shares (Exact value without rounding the number).
  - **`ops_decimal_per_game`** (number, decimal) - Offensive Point Shares (Exact value without rounding the number) per game. 
  - **`dps`** (number, decimal) - Defensive Point Shares - an estimate of the number of points contributed by a player due to his defense.
  - **`dps_per_game`** (number, decimal) - Defensive Point Shares per game. 
  - **`dps_decimal`** (number, decimal) - Defensive Point Shares (Exact value without rounding the number).
  - **`dps_decimal_per_game`** (number, decimal) -  Defensive Point Shares (Exact value without rounding the number) per game. 
  - **`ps`** (number, decimal) - Point Shares - an estimate of the number of points contributed by a player.
  - **`ps_per_game`** (number, decimal) - Point Shares per game. 
  - **`ps_decimal`** (number, decimal) - Point Shares (Exact value without rounding the number).
  - **`ps_decimal_per_game`** (number, decimal) - Point Shares (Exact value without rounding the number) per game.
  - **`shootouts_att`** (integer) - Shootout attempts. (2007–08 and later season)
  - **`shootouts_att_per_game`** (number, decimal) - Shootout attempts per game. (2007–08 and later season)
  - **`shootouts_made`** (integer) - Shootout shots made. (2007–08 and later season)
  - **`shootouts_made_per_game`** (number, decimal) - Shootout shots made per game. (2007–08 and later season)
  - **`shootouts_miss`** (integer) - Shootout shots missed. (2007–08 and later season)
  - **`shootouts_miss_per_game`** (number, decimal) - Shootout shots missed per game. (2007–08 and later season)
  - **`shootouts_made_pct`** (number, decimal) - Percentage of shootout attempts converted. (2007–08 and later season)
  - **`shootouts_made_pct_per_game`** (number, decimal) - Percentage of shootout attempts converted per game. (2007–08 and later season)
  - **`shootouts_made_pct_decimal`** (number, decimal) - Percentage of shootout attempts converted as a decimal (e.g., 0.370). (2007–08 and later season)
  - **`shootouts_made_pct_decimal_per_game`** (number, decimal) - Percentage of shootout attempts converted as a decimal per game. (2007–08 and later season)
  - **`ev_exp_on_goals_for`** (number, decimal) - 'Expected Goals For' given where shots came from, for and against, while this player was on the ice at even strength. It's based on where the shots are coming from, compared to the league-wide shooting percentage for that shot location. (2014–15 and later season)
  - **`ev_exp_on_goals_for_per_game`** (number, decimal) - Expected Goals For per game. (2014–15 and later season)
  - **`ev_exp_on_goals_against`** (number, decimal) - 'Expected Goals Against' given where shots came from, for and against, while this player was on the ice at even strength. It's based on where the shots are coming from, compared to the league-wide shooting percentage for that shot location. (2014–15 and later season)
  - **`ev_exp_on_goals_against_per_game`** (number, decimal) - Expected Goals Against per game. (2014–15 and later season)
  - **`expected_plsmns`** (number, decimal) - 'Expected +/-' given where shots came from, for and against, while this player was on the ice at even strength. It's based on where the shots are coming from, compared to the league-wide shooting percentage for that shot location. (2014–15 and later season)
  - **`expected_plsmns_per_game`** (number, decimal) - Expected +/- per game. (2014–15 and later season)
  - **`awards`** (string) - List of any individual awards received.

> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played.**
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_regular_season_20212022/position/RW/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_regular_season_now/position/RW/
```
<a name="miscellaneous_stats_players_playoff_{year}"></a>
### 2.27 Get miscellaneous stats players playoff by year
- **Endpoint:** `/miscellaneous_stats_players_playoff_{year}/`
- **Method:** GET
- **Description:** Returns a table of miscellaneous individual NHL player statistics for the specified playoff. Each object represents a player's advanced and miscellaneous stats profile for that season, such as adjusted goals, expected plus-minus, point shares, shootout data, and more. 
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`total_goals_for`** (integer) - Total Goals On-Ice For.
  - **`total_goals_for_per_game`** (number, decimal) - Total Goals On-Ice For per game. 
  - **`power_play_goals_for`** (integer) - Power play goals for while the player was on the ice.
  - **`power_play_goals_for_per_game`** (number, decimal) - Power play goals per game.
  - **`total_goals_against`** (integer) - Total Goals On-Ice Against.
  - **`total_goals_against_per_game`** (number, decimal) -  Total Goals On-Ice Against per game.
  - **`power_play_goals_against`** (integer) - Power play goals against while the player was on the ice.
  - **`power_play_goals_against_per_game`** (number, decimal) - Power play goals against per game. 
  - **`xpm`** (integer) - Plus/Minus.
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game. 
  - **`awards`** (string) - List of any individual awards received.

> [!NOTE]
> **Table data from the 2007-2008 season.**
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_playoff_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_playoff_now/
```
<a name="miscellaneous_stats_players_playoff_{year}/rank/{rank}"></a>
### 2.28 Get miscellaneous stats players playoff by year and specific rank
- **Endpoint:** `/miscellaneous_stats_players_playoff_{year}/rank/{rank}/`
- **Method:** GET
- **Description:** Returns a table of miscellaneous individual NHL player statistics for the specified playoff by specific rank. Each object represents a player's advanced and miscellaneous stats profile for that season, such as adjusted goals, expected plus-minus, point shares, shootout data, and more. 
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{rank}`** (integer) - Rank in the leaderboard, first place is the best.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`total_goals_for`** (integer) - Total Goals On-Ice For.
  - **`total_goals_for_per_game`** (number, decimal) - Total Goals On-Ice For per game. 
  - **`power_play_goals_for`** (integer) - Power play goals for while the player was on the ice.
  - **`power_play_goals_for_per_game`** (number, decimal) - Power play goals per game.
  - **`total_goals_against`** (integer) - Total Goals On-Ice Against.
  - **`total_goals_against_per_game`** (number, decimal) -  Total Goals On-Ice Against per game.
  - **`power_play_goals_against`** (integer) - Power play goals against while the player was on the ice.
  - **`power_play_goals_against_per_game`** (number, decimal) - Power play goals against per game. 
  - **`xpm`** (integer) - Plus/Minus.
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game. 
  - **`awards`** (string) - List of any individual awards received.

> [!NOTE]
> **Table data from the 2007-2008 season.**
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_playoff_20212022/rank/12
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_playoff_now/rank/12
```
<a name="miscellaneous_stats_players_playoff_{year}/team_abbrev/{team_abbrev}"></a>
### 2.29 Get miscellaneous stats players playoff by year and specific team
- **Endpoint:** `/miscellaneous_stats_players_playoff_{year}/team_abbrev/{team_abbrev}/`
- **Method:** GET
- **Description:** Returns a table of miscellaneous individual NHL player statistics for the specified playoff by specific team. Each object represents a player's advanced and miscellaneous stats profile for that season, such as adjusted goals, expected plus-minus, point shares, shootout data, and more. 
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{team_abbrev}`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`total_goals_for`** (integer) - Total Goals On-Ice For.
  - **`total_goals_for_per_game`** (number, decimal) - Total Goals On-Ice For per game. 
  - **`power_play_goals_for`** (integer) - Power play goals for while the player was on the ice.
  - **`power_play_goals_for_per_game`** (number, decimal) - Power play goals per game.
  - **`total_goals_against`** (integer) - Total Goals On-Ice Against.
  - **`total_goals_against_per_game`** (number, decimal) -  Total Goals On-Ice Against per game.
  - **`power_play_goals_against`** (integer) - Power play goals against while the player was on the ice.
  - **`power_play_goals_against_per_game`** (number, decimal) - Power play goals against per game. 
  - **`xpm`** (integer) - Plus/Minus.
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game. 
  - **`awards`** (string) - List of any individual awards received.

> [!NOTE]
> **Table data from the 2007-2008 season.**
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_playoff_20212022/team_abbrev/BOS/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_playoff_now/team_abbrev/BOS/
```
<a name="miscellaneous_stats_players_playoff_{year}/player_id/{player_id}"></a>
### 2.30 Get miscellaneous stats players playoff by year and player ID
- **Endpoint:** `/miscellaneous_stats_players_playoff_{year}/player_id/{player_id}/`
- **Method:** GET
- **Description:** Returns a table of miscellaneous individual NHL player statistics for the specified playoff by player ID. Each object represents a player's advanced and miscellaneous stats profile for that season, such as adjusted goals, expected plus-minus, point shares, shootout data, and more. 
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{player_id}`** (string) - Unique identifier for each player, contains letters and numbers.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`total_goals_for`** (integer) - Total Goals On-Ice For.
  - **`total_goals_for_per_game`** (number, decimal) - Total Goals On-Ice For per game. 
  - **`power_play_goals_for`** (integer) - Power play goals for while the player was on the ice.
  - **`power_play_goals_for_per_game`** (number, decimal) - Power play goals per game.
  - **`total_goals_against`** (integer) - Total Goals On-Ice Against.
  - **`total_goals_against_per_game`** (number, decimal) -  Total Goals On-Ice Against per game.
  - **`power_play_goals_against`** (integer) - Power play goals against while the player was on the ice.
  - **`power_play_goals_against_per_game`** (number, decimal) - Power play goals against per game. 
  - **`xpm`** (integer) - Plus/Minus.
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game. 
  - **`awards`** (string) - List of any individual awards received.

> [!NOTE]
> **Table data from the 2007-2008 season.**
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_playoff_20212022/player_id/acciano01/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_playoff_now/player_id/acciano01/
```
<a name="miscellaneous_stats_players_playoff_{year}/position/{position}"></a>
### 2.31 Get miscellaneous stats players playoff by year and position
- **Endpoint:** `/miscellaneous_stats_players_playoff_{year}/position/{position}/`
- **Method:** GET
- **Description:** Returns a table of miscellaneous individual NHL player statistics for the specified playoff by position. Each object represents a player's advanced and miscellaneous stats profile for that season, such as adjusted goals, expected plus-minus, point shares, shootout data, and more. 
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{position}`** (string) - Primary position played (C, LW, RW, D).
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`total_goals_for`** (integer) - Total Goals On-Ice For.
  - **`total_goals_for_per_game`** (number, decimal) - Total Goals On-Ice For per game. 
  - **`power_play_goals_for`** (integer) - Power play goals for while the player was on the ice.
  - **`power_play_goals_for_per_game`** (number, decimal) - Power play goals per game.
  - **`total_goals_against`** (integer) - Total Goals On-Ice Against.
  - **`total_goals_against_per_game`** (number, decimal) -  Total Goals On-Ice Against per game.
  - **`power_play_goals_against`** (integer) - Power play goals against while the player was on the ice.
  - **`power_play_goals_against_per_game`** (number, decimal) - Power play goals against per game. 
  - **`xpm`** (integer) - Plus/Minus.
  - **`xpm_per_game`** (number, decimal) - Plus/Minus per game. 
  - **`awards`** (string) - List of any individual awards received.

> [!NOTE]
> **Table data from the 2007-2008 season.**
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_playoff_20212022/position/RW/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/miscellaneous_stats_players_playoff_now/position/RW/
```
<a name="hat_tricks_{year}"></a>
### 2.32 Get hat tricks by year
- **Endpoint:** `/hat_tricks_{year}/`
- **Method:** GET
- **Description:** Returns a table of detailed information about all NHL hat tricks for a given season.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`game_date`** (date) - Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_id`** (string) - Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`opponent`** (string) - Opponent abbreviation (e.g., EDM, NYR, TOR).
  - **`goal`** (integer) - Number of goals scored in this match. 
  - **`score`** (string) - Total game score.
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/hat_tricks_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/hat_tricks_now/
```
<a name="hat_tricks_{year}/team_abbrev/{team_abbrev}"></a>
### 2.33 Get hat tricks by year and specific team
- **Endpoint:** `/hat_tricks_{year}/team_abbrev/{team_abbrev}/`
- **Method:** GET
- **Description:** Returns a table of detailed information about all NHL hat tricks for a given season by and specific team.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{team_abbrev}`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`game_date`** (date) - Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_id`** (string) - Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`opponent`** (string) - Opponent abbreviation (e.g., EDM, NYR, TOR).
  - **`goal`** (integer) - Number of goals scored in this match. 
  - **`score`** (string) - Total game score.
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/hat_tricks_20212022/team_abbrev/BOS/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/hat_tricks_now/team_abbrev/BOS/
```
<a name="hat_tricks_{year}/player_id/{player_id}"></a>
### 2.34 Get hat tricks by year and player ID
- **Endpoint:** `/hat_tricks_{year}/player_id/{player_id}/`
- **Method:** GET
- **Description:** Returns a table of detailed information about all NHL hat tricks for a given season by and player ID.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{player_id}`** (string) - Unique identifier for each player, contains letters and numbers.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`game_date`** (date) - Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_id`** (string) - Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`opponent`** (string) - Opponent abbreviation (e.g., EDM, NYR, TOR).
  - **`goal`** (integer) - Number of goals scored in this match. 
  - **`score`** (string) - Total game score.
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/hat_tricks_20212022/player_id/bennesa01/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/hat_tricks_now/player_id/bennesa01/
```
<a name="hat_tricks_{year}/game_id/{game_id}"></a>
### 2.35 Get hat tricks by year and specific game
- **Endpoint:** `/hat_tricks_{year}/game_id/{game_id}/`
- **Method:** GET
- **Description:** Returns a table of detailed information about all NHL hat tricks for a given season by and specific game.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{game_id}`** (string) - Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`game_date`** (date) - Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_id`** (string) - Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`opponent`** (string) - Opponent abbreviation (e.g., EDM, NYR, TOR).
  - **`goal`** (integer) - Number of goals scored in this match. 
  - **`score`** (string) - Total game score.
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/hat_tricks_20212022/game_id/202110160FLA/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/hat_tricks_now/game_id/202110160FLA/
```
<a name="hat_tricks_{year}/game_date/{game_date}"></a>
### 2.36 Get hat tricks by year and specific date
- **Endpoint:** `/hat_tricks_{year}/game_date/{game_date}/`
- **Method:** GET
- **Description:** Returns a table of detailed information about all NHL hat tricks for a given season by and specific date.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{game_date}`** (date) - Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`game_date`** (date) - Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_id`** (string) - Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`opponent`** (string) - Opponent abbreviation (e.g., EDM, NYR, TOR).
  - **`goal`** (integer) - Number of goals scored in this match. 
  - **`score`** (string) - Total game score.
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/hat_tricks_20212022/game_date/2021-10-16/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/hat_tricks_now/game_date/2021-10-16/
```
<a name="penalty_shots_{year}"></a>
### 2.37 Get penalty shots by year
- **Endpoint:** `/penalty_shots_{year}/`
- **Method:** GET
- **Description:** Returns a table of detailed information about all NHL penalty shots for a given season.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`game_date`** (date) - Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_id`** (string) - Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`opponent`** (string) - Opponent abbreviation (e.g., EDM, NYR, TOR).
  - **`goal`** (string) - Only two meanings "goal" or "miss". 
  - **`score`** (string) - Total game score.
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/penalty_shots_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/penalty_shots_now/
```
<a name="penalty_shots_{year}/team_abbrev/{team_abbrev}"></a>
### 2.38 Get penalty shots by year and specific team
- **Endpoint:** `/penalty_shots_{year}/team_abbrev/{team_abbrev}/`
- **Method:** GET
- **Description:** Returns a table of detailed information about all NHL penalty shots for a given season by and specific team.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{team_abbrev}`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`game_date`** (date) - Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_id`** (string) - Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`opponent`** (string) - Opponent abbreviation (e.g., EDM, NYR, TOR).
  - **`goal`** (string) - Only two meanings "goal" or "miss". 
  - **`score`** (string) - Total game score.
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/penalty_shots_20212022/team_abbrev/BOS/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/penalty_shots_now/team_abbrev/BOS/
```
<a name="penalty_shots_{year}/player_id/{player_id}"></a>
### 2.39 Get penalty shots by year and player ID
- **Endpoint:** `/penalty_shots_{year}/player_id/{player_id}/`
- **Method:** GET
- **Description:** Returns a table of detailed information about all NHL penalty shots for a given season by and player ID.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{player_id}`** (string) - Unique identifier for each player, contains letters and numbers.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`game_date`** (date) - Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_id`** (string) - Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`opponent`** (string) - Opponent abbreviation (e.g., EDM, NYR, TOR).
  - **`goal`** (string) - Only two meanings "goal" or "miss". 
  - **`score`** (string) - Total game score.
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/penalty_shots_20212022/player_id/laughsc01/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/penalty_shots_now/player_id/laughsc01/
```
<a name="penalty_shots_{year}/game_id/{game_id}"></a>
### 2.40 Get penalty shots by year and specific game
- **Endpoint:** `/penalty_shots_{year}/game_id/{game_id}/`
- **Method:** GET
- **Description:** Returns a table of detailed information about all NHL penalty shots for a given season by and specific game.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{game_id}`** (string) - Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`game_date`** (date) - Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_id`** (string) - Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`opponent`** (string) - Opponent abbreviation (e.g., EDM, NYR, TOR).
  - **`goal`** (string) - Only two meanings "goal" or "miss".
  - **`score`** (string) - Total game score.
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/penalty_shots_20212022/game_id/202111160PHI/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/penalty_shots_now/game_id/202111160PHI/
```
<a name="penalty shots_{year}/game_date/{game_date}"></a>
### 2.41 Get penalty shots by year and specific date
- **Endpoint:** `/penalty_shots_{year}/game_date/{game_date}/`
- **Method:** GET
- **Description:** Returns a table of detailed information about all NHL penalty shots for a given season by and specific date.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{game_date}`** (date) - Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`game_date`** (date) - Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_id`** (string) - Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`opponent`** (string) - Opponent abbreviation (e.g., EDM, NYR, TOR).
  - **`goal`** (string) - Only two meanings "goal" or "miss".
  - **`score`** (string) - Total game score.
    
##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/penalty_shots_20212022/game_date/2021-11-16/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/penalty_shots_now/game_date/2021-11-16/
```
<a name="advanced_stats_players_{year}"></a>
### 2.42 Get advanced stats players by year
- **Endpoint:** `/advanced_stats_players_{year}/`
- **Method:** GET
- **Description:** Returns a table of advanced individual player statistics for the specified NHL season. Each object represents a player’s statistical profile for that season. Data start from 2007–08 season.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`corsi_for`** (integer) - Corsi For at Even Strength (Shots + Blocks + Misses).
  - **`corsi_against`** (integer) - Corsi Against at Even Strength (Shots + Blocks + Misses).
  - **`corsi_pct`** (number, decimal) - Corsi For % at Even Strength corsi_for / (corsi_for + corsi_against) . Above 50% means the team was controlling the puck more often than not with this player on the<br>ice in this situation.
  - **`corsi_rel_pct`** (number, decimal) - Relative Corsi For % at Even Strength .On-Ice Corsi For % - Off-Ice Corsi For %.
  - **`fenwick_for`** (integer) - Fenwick For at Even Strength (Shots + Misses).
  - **`fenwick_against`** (integer) - Fenwick Against at Even Strength (Shots + Misses).
  - **`fenwick_pct`** (number, decimal) - Fenwick For % at Even Strength fenwick_for / (fenwick_for + fenwick_against) .Above 50% means the team was controlling the<br>puck more often than not with this player on the ice in this situation.
  - **`fenwick_rel_pct`** (number, decimal) - Relative Fenwick For %. On-Ice Fenwick For % - Off-Ice Fenwick For %.
  - **`on_ice_shot_pct`** (number, decimal) - Team On-Ice Shooting Percentage . Shooting % while this player/team was on the ice.
  - **`on_ice_sv_pct`** (number, decimal) - Team On-Ice Save Percentage . Save % while this player/team was on the ice.
  - **`pdo`** (number, decimal) - PDO. Shooting % + Save %.
  - **`zs_offense_pct`** (number, decimal) - Offensive Zone Start % . Offensive Zone Faceoffs / (Offensive Zone Faceoffs + Defensive Zone Faceoffs), that took place while on the ice.
  - **`zs_defense_pct`** (number, decimal) - Defensive Zone Start %. Defensive Zone Faceoffs / (Offensive Zone Faceoffs + Defensive Zone Faceoffs), that took place while on the ice.
  - **`toi_pbp_per_60_all`** (string) - TOI/60 in All Situations. Time on Ice per 60 minutes.
  - **`toi_pbp_per_60_all_decimal`** (number, decimal) - TOI/60 in All Situations. Time on Ice per 60 minutes (number, decimal).
  - **`toi_pbp_per_60_ev`** (string) - TOI/60 at Even Strength. Time on Ice per 60 minutes.
  - **`toi_pbp_per_60_ev_decimal`** (number, decimal) - TOI/60 at Even Strength. Time on Ice per 60 minutes (number, decimal).
  - **`take`** (integer) - Takeaways.
  - **`give`** (integer) - Giveaways.
  - **`total_shots_attempted_all`** (integer) - Total shots attempted in all situations.
  - **`shot_thru_percentage`** (number, decimal) - Percentage of shots taken that go on net.
    
> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played. Data start from 2007-08 season**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/advanced_stats_players_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/advanced_stats_players_now/
```
<a name="advanced_stats_players_{year}/rank/{rank}"></a>
### 2.43 Get advanced stats players by year and specific rank
- **Endpoint:** `/advanced_stats_players_{year}/rank/{rank}/`
- **Method:** GET
- **Description:** Returns a table of advanced individual player statistics for the specified NHL season and specific rank. Each object represents a player’s statistical profile for that season. Data start from 2007–08 season.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{rank}`** (integer) - Rank in the leaderboard, first place is the best.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`corsi_for`** (integer) - Corsi For at Even Strength (Shots + Blocks + Misses).
  - **`corsi_against`** (integer) - Corsi Against at Even Strength (Shots + Blocks + Misses).
  - **`corsi_pct`** (number, decimal) - Corsi For % at Even Strength corsi_for / (corsi_for + corsi_against) . Above 50% means the team was controlling the puck more often than not with this player on the<br>ice in this situation.
  - **`corsi_rel_pct`** (number, decimal) - Relative Corsi For % at Even Strength .On-Ice Corsi For % - Off-Ice Corsi For %.
  - **`fenwick_for`** (integer) - Fenwick For at Even Strength (Shots + Misses).
  - **`fenwick_against`** (integer) - Fenwick Against at Even Strength (Shots + Misses).
  - **`fenwick_pct`** (number, decimal) - Fenwick For % at Even Strength fenwick_for / (fenwick_for + fenwick_against) .Above 50% means the team was controlling the<br>puck more often than not with this player on the ice in this situation.
  - **`fenwick_rel_pct`** (number, decimal) - Relative Fenwick For %. On-Ice Fenwick For % - Off-Ice Fenwick For %.
  - **`on_ice_shot_pct`** (number, decimal) - Team On-Ice Shooting Percentage . Shooting % while this player/team was on the ice.
  - **`on_ice_sv_pct`** (number, decimal) - Team On-Ice Save Percentage . Save % while this player/team was on the ice.
  - **`pdo`** (number, decimal) - PDO. Shooting % + Save %.
  - **`zs_offense_pct`** (number, decimal) - Offensive Zone Start % . Offensive Zone Faceoffs / (Offensive Zone Faceoffs + Defensive Zone Faceoffs), that took place while on the ice.
  - **`zs_defense_pct`** (number, decimal) - Defensive Zone Start %. Defensive Zone Faceoffs / (Offensive Zone Faceoffs + Defensive Zone Faceoffs), that took place while on the ice.
  - **`toi_pbp_per_60_all`** (string) - TOI/60 in All Situations. Time on Ice per 60 minutes.
  - **`toi_pbp_per_60_all_decimal`** (number, decimal) - TOI/60 in All Situations. Time on Ice per 60 minutes (number, decimal).
  - **`toi_pbp_per_60_ev`** (string) - TOI/60 at Even Strength. Time on Ice per 60 minutes.
  - **`toi_pbp_per_60_ev_decimal`** (number, decimal) - TOI/60 at Even Strength. Time on Ice per 60 minutes (number, decimal).
  - **`take`** (integer) - Takeaways.
  - **`give`** (integer) - Giveaways.
  - **`total_shots_attempted_all`** (integer) - Total shots attempted in all situations.
  - **`shot_thru_percentage`** (number, decimal) - Percentage of shots taken that go on net.
    
> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played. Data start from 2007-08 season**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/advanced_stats_players_20212022/rank/23/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/advanced_stats_players_now/rank/23/
```
<a name="advanced_stats_players_{year}/player_id/{player_id}"></a>
### 2.44 Get advanced stats players by year and player ID
- **Endpoint:** `/advanced_stats_players_{year}/player_id/{player_id}/`
- **Method:** GET
- **Description:** Returns a table of advanced individual player statistics for the specified NHL season and player ID. Each object represents a player’s statistical profile for that season. Data start from 2007–08 season.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{rank}`** (integer) - Rank in the leaderboard, first place is the best.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`corsi_for`** (integer) - Corsi For at Even Strength (Shots + Blocks + Misses).
  - **`corsi_against`** (integer) - Corsi Against at Even Strength (Shots + Blocks + Misses).
  - **`corsi_pct`** (number, decimal) - Corsi For % at Even Strength corsi_for / (corsi_for + corsi_against) . Above 50% means the team was controlling the puck more often than not with this player on the<br>ice in this situation.
  - **`corsi_rel_pct`** (number, decimal) - Relative Corsi For % at Even Strength .On-Ice Corsi For % - Off-Ice Corsi For %.
  - **`fenwick_for`** (integer) - Fenwick For at Even Strength (Shots + Misses).
  - **`fenwick_against`** (integer) - Fenwick Against at Even Strength (Shots + Misses).
  - **`fenwick_pct`** (number, decimal) - Fenwick For % at Even Strength fenwick_for / (fenwick_for + fenwick_against) .Above 50% means the team was controlling the<br>puck more often than not with this player on the ice in this situation.
  - **`fenwick_rel_pct`** (number, decimal) - Relative Fenwick For %. On-Ice Fenwick For % - Off-Ice Fenwick For %.
  - **`on_ice_shot_pct`** (number, decimal) - Team On-Ice Shooting Percentage . Shooting % while this player/team was on the ice.
  - **`on_ice_sv_pct`** (number, decimal) - Team On-Ice Save Percentage . Save % while this player/team was on the ice.
  - **`pdo`** (number, decimal) - PDO. Shooting % + Save %.
  - **`zs_offense_pct`** (number, decimal) - Offensive Zone Start % . Offensive Zone Faceoffs / (Offensive Zone Faceoffs + Defensive Zone Faceoffs), that took place while on the ice.
  - **`zs_defense_pct`** (number, decimal) - Defensive Zone Start %. Defensive Zone Faceoffs / (Offensive Zone Faceoffs + Defensive Zone Faceoffs), that took place while on the ice.
  - **`toi_pbp_per_60_all`** (string) - TOI/60 in All Situations. Time on Ice per 60 minutes.
  - **`toi_pbp_per_60_all_decimal`** (number, decimal) - TOI/60 in All Situations. Time on Ice per 60 minutes (number, decimal).
  - **`toi_pbp_per_60_ev`** (string) - TOI/60 at Even Strength. Time on Ice per 60 minutes.
  - **`toi_pbp_per_60_ev_decimal`** (number, decimal) - TOI/60 at Even Strength. Time on Ice per 60 minutes (number, decimal).
  - **`take`** (integer) - Takeaways.
  - **`give`** (integer) - Giveaways.
  - **`total_shots_attempted_all`** (integer) - Total shots attempted in all situations.
  - **`shot_thru_percentage`** (number, decimal) - Percentage of shots taken that go on net.
    
> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played. Data start from 2007-08 season**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/advanced_stats_players_20212022/player_id/ahose01/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/advanced_stats_players_now/player_id/ahose01/
```
<a name="advanced_stats_players_{year}/team_abbrev/{team_abbrev}"></a>
### 2.45 Get advanced stats players by year and specific team
- **Endpoint:** `/advanced_stats_players_{year}/team_abbrev/{team_abbrev}/`
- **Method:** GET
- **Description:** Returns a table of advanced individual player statistics for the specified NHL season and specific team. Each object represents a player’s statistical profile for that season. Data start from 2007–08 season.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{team_abbrev}`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`corsi_for`** (integer) - Corsi For at Even Strength (Shots + Blocks + Misses).
  - **`corsi_against`** (integer) - Corsi Against at Even Strength (Shots + Blocks + Misses).
  - **`corsi_pct`** (number, decimal) - Corsi For % at Even Strength corsi_for / (corsi_for + corsi_against) . Above 50% means the team was controlling the puck more often than not with this player on the<br>ice in this situation.
  - **`corsi_rel_pct`** (number, decimal) - Relative Corsi For % at Even Strength .On-Ice Corsi For % - Off-Ice Corsi For %.
  - **`fenwick_for`** (integer) - Fenwick For at Even Strength (Shots + Misses).
  - **`fenwick_against`** (integer) - Fenwick Against at Even Strength (Shots + Misses).
  - **`fenwick_pct`** (number, decimal) - Fenwick For % at Even Strength fenwick_for / (fenwick_for + fenwick_against) .Above 50% means the team was controlling the<br>puck more often than not with this player on the ice in this situation.
  - **`fenwick_rel_pct`** (number, decimal) - Relative Fenwick For %. On-Ice Fenwick For % - Off-Ice Fenwick For %.
  - **`on_ice_shot_pct`** (number, decimal) - Team On-Ice Shooting Percentage . Shooting % while this player/team was on the ice.
  - **`on_ice_sv_pct`** (number, decimal) - Team On-Ice Save Percentage . Save % while this player/team was on the ice.
  - **`pdo`** (number, decimal) - PDO. Shooting % + Save %.
  - **`zs_offense_pct`** (number, decimal) - Offensive Zone Start % . Offensive Zone Faceoffs / (Offensive Zone Faceoffs + Defensive Zone Faceoffs), that took place while on the ice.
  - **`zs_defense_pct`** (number, decimal) - Defensive Zone Start %. Defensive Zone Faceoffs / (Offensive Zone Faceoffs + Defensive Zone Faceoffs), that took place while on the ice.
  - **`toi_pbp_per_60_all`** (string) - TOI/60 in All Situations. Time on Ice per 60 minutes.
  - **`toi_pbp_per_60_all_decimal`** (number, decimal) - TOI/60 in All Situations. Time on Ice per 60 minutes (number, decimal).
  - **`toi_pbp_per_60_ev`** (string) - TOI/60 at Even Strength. Time on Ice per 60 minutes.
  - **`toi_pbp_per_60_ev_decimal`** (number, decimal) - TOI/60 at Even Strength. Time on Ice per 60 minutes (number, decimal).
  - **`take`** (integer) - Takeaways.
  - **`give`** (integer) - Giveaways.
  - **`total_shots_attempted_all`** (integer) - Total shots attempted in all situations.
  - **`shot_thru_percentage`** (number, decimal) - Percentage of shots taken that go on net.
    
> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played. Data start from 2007-08 season**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/advanced_stats_players_20212022/team_abbrev/BOS/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/advanced_stats_players_now/team_abbrev/BOS/
```
<a name="advanced_stats_players_{year}/position/{position}"></a>
### 2.46 Get advanced stats players by year and position
- **Endpoint:** `/advanced_stats_players_{year}/position/{position}/`
- **Method:** GET
- **Description:** Returns a table of advanced individual player statistics for the specified NHL season and position. Each object represents a player’s statistical profile for that season. Data start from 2007–08 season.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{posittion}`** (string) - Primary position played (C, LW, RW, D).
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`age`** (integer) - Player's age of the season.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`games_played`** (integer) - Games played.
  - **`corsi_for`** (integer) - Corsi For at Even Strength (Shots + Blocks + Misses).
  - **`corsi_against`** (integer) - Corsi Against at Even Strength (Shots + Blocks + Misses).
  - **`corsi_pct`** (number, decimal) - Corsi For % at Even Strength corsi_for / (corsi_for + corsi_against) . Above 50% means the team was controlling the puck more often than not with this player on the<br>ice in this situation.
  - **`corsi_rel_pct`** (number, decimal) - Relative Corsi For % at Even Strength .On-Ice Corsi For % - Off-Ice Corsi For %.
  - **`fenwick_for`** (integer) - Fenwick For at Even Strength (Shots + Misses).
  - **`fenwick_against`** (integer) - Fenwick Against at Even Strength (Shots + Misses).
  - **`fenwick_pct`** (number, decimal) - Fenwick For % at Even Strength fenwick_for / (fenwick_for + fenwick_against) .Above 50% means the team was controlling the<br>puck more often than not with this player on the ice in this situation.
  - **`fenwick_rel_pct`** (number, decimal) - Relative Fenwick For %. On-Ice Fenwick For % - Off-Ice Fenwick For %.
  - **`on_ice_shot_pct`** (number, decimal) - Team On-Ice Shooting Percentage . Shooting % while this player/team was on the ice.
  - **`on_ice_sv_pct`** (number, decimal) - Team On-Ice Save Percentage . Save % while this player/team was on the ice.
  - **`pdo`** (number, decimal) - PDO. Shooting % + Save %.
  - **`zs_offense_pct`** (number, decimal) - Offensive Zone Start % . Offensive Zone Faceoffs / (Offensive Zone Faceoffs + Defensive Zone Faceoffs), that took place while on the ice.
  - **`zs_defense_pct`** (number, decimal) - Defensive Zone Start %. Defensive Zone Faceoffs / (Offensive Zone Faceoffs + Defensive Zone Faceoffs), that took place while on the ice.
  - **`toi_pbp_per_60_all`** (string) - TOI/60 in All Situations. Time on Ice per 60 minutes.
  - **`toi_pbp_per_60_all_decimal`** (number, decimal) - TOI/60 in All Situations. Time on Ice per 60 minutes (number, decimal).
  - **`toi_pbp_per_60_ev`** (string) - TOI/60 at Even Strength. Time on Ice per 60 minutes.
  - **`toi_pbp_per_60_ev_decimal`** (number, decimal) - TOI/60 at Even Strength. Time on Ice per 60 minutes (number, decimal).
  - **`take`** (integer) - Takeaways.
  - **`give`** (integer) - Giveaways.
  - **`total_shots_attempted_all`** (integer) - Total shots attempted in all situations.
  - **`shot_thru_percentage`** (number, decimal) - Percentage of shots taken that go on net.
    
> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played. Data start from 2007-08 season**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/advanced_stats_players_20212022/position/RW/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/advanced_stats_players_now/position/RW/
```
<a name="skater_time_on_ice_stats_{year}"></a>
### 2.47 Get skater time on ice stats by year
- **Endpoint:** `/skater_time_on_ice_stats_{year}/`
- **Method:** GET
- **Description:** Returns a table of skater time on ice stats for the specified NHL season. Each object represents a player’s statistical profile for that season. Data start from 2007–08 season.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`avg_shift_length`** (string) - Avg. Shift Length/Gm (hh:mm).
  - **`avg_shift_length_decimal`** (number, decimal) - Avg. Shift Length/Gm (hh:mm). (number, decimal)
  - **`games_played`** (integer) - Games played.
  - **`toi_ev`** (string) - Avg. Time on Ice/Gm at Even Strength.
  - **`toi_ev_decimal`** (number, decimal) - Avg. Time on Ice/Gm at Even Strength. (number, decimal)
  - **`corsi_rel_pct_ev`** (number, decimal) - Relative Corsi For % at Even Strength.
  - **`on_gf_per_60_ev`** (number, decimal) - On-Ice Goals For/60 Minutes at Even Strength.
  - **`on_ga_per_60_ev`** (number, decimal) - On-Ice Goals Against/60 Minutes at Even Strength.
  - **`toi_pp`** (string) - Avg. Time on Ice/Gm while on Power Play.
  - **`toi_pp_decimal`** (number, decimal) - Avg. Time on Ice/Gm while on Power Play. (number, decimal)
  - **`corsi_rel_pct_pp`** (number, decimal) - Relative Corsi For % on the Power Play.
  - **`on_gf_per_60_pp`** (number, decimal) - On-Ice Goals For/60 Minutes on the Power Play.
  - **`on_ga_per_60_pp`** (number, decimal) - On-Ice Goals Against/60 Minutes on the Power Play.
  - **`toi_sh`** (string) - Avg. Time on Ice/Gm while Short Handed.
  - **`toi_sh_decimal`** (number, decimal) -  Avg. Time on Ice/Gm while Short Handed. (number, decimal)
  - **`corsi_rel_pct_sh`** (number, decimal) - Relative Corsi For % while Short Handed.
  - **`on_gf_per_60_sh`** (number, decimal) - On-Ice Goals For/60 Minutes while Short Handed.
  - **`on_ga_per_60_sh`** (number, decimal) - On-Ice Goals Against/60 Minutes while Short Handed.
    
> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played. Data start from 2007-08 season**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/skater_time_on_ice_stats_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/skater_time_on_ice_stats_now/
```
<a name="skater_time_on_ice_stats_{year}/rank/{rank}"></a>
### 2.48 Get skater time on ice stats by year and specific rank
- **Endpoint:** `/skater_time_on_ice_stats_{year}/rank/{rank}/`
- **Method:** GET
- **Description:** Returns a table of skater time on ice stats for the specified NHL season and specific rank. Each object represents a player’s statistical profile for that season. Data start from 2007–08 season.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{rank}`** (integer) - Rank in the leaderboard, first place is the best.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`avg_shift_length`** (string) - Avg. Shift Length/Gm (hh:mm).
  - **`avg_shift_length_decimal`** (number, decimal) - Avg. Shift Length/Gm (hh:mm). (number, decimal)
  - **`games_played`** (integer) - Games played.
  - **`toi_ev`** (string) - Avg. Time on Ice/Gm at Even Strength.
  - **`toi_ev_decimal`** (number, decimal) - Avg. Time on Ice/Gm at Even Strength. (number, decimal)
  - **`corsi_rel_pct_ev`** (number, decimal) - Relative Corsi For % at Even Strength.
  - **`on_gf_per_60_ev`** (number, decimal) - On-Ice Goals For/60 Minutes at Even Strength.
  - **`on_ga_per_60_ev`** (number, decimal) - On-Ice Goals Against/60 Minutes at Even Strength.
  - **`toi_pp`** (string) - Avg. Time on Ice/Gm while on Power Play.
  - **`toi_pp_decimal`** (number, decimal) - Avg. Time on Ice/Gm while on Power Play. (number, decimal)
  - **`corsi_rel_pct_pp`** (number, decimal) - Relative Corsi For % on the Power Play.
  - **`on_gf_per_60_pp`** (number, decimal) - On-Ice Goals For/60 Minutes on the Power Play.
  - **`on_ga_per_60_pp`** (number, decimal) - On-Ice Goals Against/60 Minutes on the Power Play.
  - **`toi_sh`** (string) - Avg. Time on Ice/Gm while Short Handed.
  - **`toi_sh_decimal`** (number, decimal) -  Avg. Time on Ice/Gm while Short Handed. (number, decimal)
  - **`corsi_rel_pct_sh`** (number, decimal) - Relative Corsi For % while Short Handed.
  - **`on_gf_per_60_sh`** (number, decimal) - On-Ice Goals For/60 Minutes while Short Handed.
  - **`on_ga_per_60_sh`** (number, decimal) - On-Ice Goals Against/60 Minutes while Short Handed.
    
> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played. Data start from 2007-08 season**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/skater_time_on_ice_stats_20212022/rank/22/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/skater_time_on_ice_stats_now/rank/22/
```
<a name="skater_time_on_ice_stats_{year}/player_id/{player_id}"></a>
### 2.49 Get skater time on ice stats by year and player ID
- **Endpoint:** `/skater_time_on_ice_stats_{year}/player_id/{player_id}/`
- **Method:** GET
- **Description:** Returns a table of skater time on ice stats for the specified NHL season and player ID. Each object represents a player’s statistical profile for that season. Data start from 2007–08 season.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{player_id}`** (string) - Unique identifier for each player, contains letters and numbers.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`avg_shift_length`** (string) - Avg. Shift Length/Gm (hh:mm).
  - **`avg_shift_length_decimal`** (number, decimal) - Avg. Shift Length/Gm (hh:mm). (number, decimal)
  - **`games_played`** (integer) - Games played.
  - **`toi_ev`** (string) - Avg. Time on Ice/Gm at Even Strength.
  - **`toi_ev_decimal`** (number, decimal) - Avg. Time on Ice/Gm at Even Strength. (number, decimal)
  - **`corsi_rel_pct_ev`** (number, decimal) - Relative Corsi For % at Even Strength.
  - **`on_gf_per_60_ev`** (number, decimal) - On-Ice Goals For/60 Minutes at Even Strength.
  - **`on_ga_per_60_ev`** (number, decimal) - On-Ice Goals Against/60 Minutes at Even Strength.
  - **`toi_pp`** (string) - Avg. Time on Ice/Gm while on Power Play.
  - **`toi_pp_decimal`** (number, decimal) - Avg. Time on Ice/Gm while on Power Play. (number, decimal)
  - **`corsi_rel_pct_pp`** (number, decimal) - Relative Corsi For % on the Power Play.
  - **`on_gf_per_60_pp`** (number, decimal) - On-Ice Goals For/60 Minutes on the Power Play.
  - **`on_ga_per_60_pp`** (number, decimal) - On-Ice Goals Against/60 Minutes on the Power Play.
  - **`toi_sh`** (string) - Avg. Time on Ice/Gm while Short Handed.
  - **`toi_sh_decimal`** (number, decimal) -  Avg. Time on Ice/Gm while Short Handed. (number, decimal)
  - **`corsi_rel_pct_sh`** (number, decimal) - Relative Corsi For % while Short Handed.
  - **`on_gf_per_60_sh`** (number, decimal) - On-Ice Goals For/60 Minutes while Short Handed.
  - **`on_ga_per_60_sh`** (number, decimal) - On-Ice Goals Against/60 Minutes while Short Handed.
    
> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played. Data start from 2007-08 season**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/skater_time_on_ice_stats_20212022/player_id/addisca01/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/skater_time_on_ice_stats_now/player_id/addisca01/
```
<a name="skater_time_on_ice_stats_{year}/team_abbrev/{team_abbrev}"></a>
### 2.50 Get skater time on ice stats by year and specific team
- **Endpoint:** `/skater_time_on_ice_stats_{year}/team_abbrev/{team_abbrev}/`
- **Method:** GET
- **Description:** Returns a table of skater time on ice stats for the specified NHL season and specific team. Each object represents a player’s statistical profile for that season. Data start from 2007–08 season.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{team_abbrev}`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`avg_shift_length`** (string) - Avg. Shift Length/Gm (hh:mm).
  - **`avg_shift_length_decimal`** (number, decimal) - Avg. Shift Length/Gm (hh:mm). (number, decimal)
  - **`games_played`** (integer) - Games played.
  - **`toi_ev`** (string) - Avg. Time on Ice/Gm at Even Strength.
  - **`toi_ev_decimal`** (number, decimal) - Avg. Time on Ice/Gm at Even Strength. (number, decimal)
  - **`corsi_rel_pct_ev`** (number, decimal) - Relative Corsi For % at Even Strength.
  - **`on_gf_per_60_ev`** (number, decimal) - On-Ice Goals For/60 Minutes at Even Strength.
  - **`on_ga_per_60_ev`** (number, decimal) - On-Ice Goals Against/60 Minutes at Even Strength.
  - **`toi_pp`** (string) - Avg. Time on Ice/Gm while on Power Play.
  - **`toi_pp_decimal`** (number, decimal) - Avg. Time on Ice/Gm while on Power Play. (number, decimal)
  - **`corsi_rel_pct_pp`** (number, decimal) - Relative Corsi For % on the Power Play.
  - **`on_gf_per_60_pp`** (number, decimal) - On-Ice Goals For/60 Minutes on the Power Play.
  - **`on_ga_per_60_pp`** (number, decimal) - On-Ice Goals Against/60 Minutes on the Power Play.
  - **`toi_sh`** (string) - Avg. Time on Ice/Gm while Short Handed.
  - **`toi_sh_decimal`** (number, decimal) -  Avg. Time on Ice/Gm while Short Handed. (number, decimal)
  - **`corsi_rel_pct_sh`** (number, decimal) - Relative Corsi For % while Short Handed.
  - **`on_gf_per_60_sh`** (number, decimal) - On-Ice Goals For/60 Minutes while Short Handed.
  - **`on_ga_per_60_sh`** (number, decimal) - On-Ice Goals Against/60 Minutes while Short Handed.
    
> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played. Data start from 2007-08 season**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/skater_time_on_ice_stats_20212022/team_abbrev/BOS/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/skater_time_on_ice_stats_now/team_abbrev/BOS/
```
<a name="skater_time_on_ice_stats_{year}/position/{position}"></a>
### 2.51 Get skater time on ice stats by year and position
- **Endpoint:** `/skater_time_on_ice_stats_{year}/position/{position}/`
- **Method:** GET
- **Description:** Returns a table of skater time on ice stats for the specified NHL season and position. Each object represents a player’s statistical profile for that season. Data start from 2007–08 season.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{posittion}`** (string) - Primary position played (C, LW, RW, D).
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Team abbreviation (e.g., EDM, NYR, TOR).
  - **`posittion`** (string) - Primary position played (C, LW, RW, D).
  - **`avg_shift_length`** (string) - Avg. Shift Length/Gm (hh:mm).
  - **`avg_shift_length_decimal`** (number, decimal) - Avg. Shift Length/Gm (hh:mm). (number, decimal)
  - **`games_played`** (integer) - Games played.
  - **`toi_ev`** (string) - Avg. Time on Ice/Gm at Even Strength.
  - **`toi_ev_decimal`** (number, decimal) - Avg. Time on Ice/Gm at Even Strength. (number, decimal)
  - **`corsi_rel_pct_ev`** (number, decimal) - Relative Corsi For % at Even Strength.
  - **`on_gf_per_60_ev`** (number, decimal) - On-Ice Goals For/60 Minutes at Even Strength.
  - **`on_ga_per_60_ev`** (number, decimal) - On-Ice Goals Against/60 Minutes at Even Strength.
  - **`toi_pp`** (string) - Avg. Time on Ice/Gm while on Power Play.
  - **`toi_pp_decimal`** (number, decimal) - Avg. Time on Ice/Gm while on Power Play. (number, decimal)
  - **`corsi_rel_pct_pp`** (number, decimal) - Relative Corsi For % on the Power Play.
  - **`on_gf_per_60_pp`** (number, decimal) - On-Ice Goals For/60 Minutes on the Power Play.
  - **`on_ga_per_60_pp`** (number, decimal) - On-Ice Goals Against/60 Minutes on the Power Play.
  - **`toi_sh`** (string) - Avg. Time on Ice/Gm while Short Handed.
  - **`toi_sh_decimal`** (number, decimal) -  Avg. Time on Ice/Gm while Short Handed. (number, decimal)
  - **`corsi_rel_pct_sh`** (number, decimal) - Relative Corsi For % while Short Handed.
  - **`on_gf_per_60_sh`** (number, decimal) - On-Ice Goals For/60 Minutes while Short Handed.
  - **`on_ga_per_60_sh`** (number, decimal) - On-Ice Goals Against/60 Minutes while Short Handed.
    
> [!NOTE]
> **Some data for some players may be NULL if this data is specific to a specific position (eg goalkeeper) or the player has not played. Data start from 2007-08 season**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/skater_time_on_ice_stats_20212022/position/RW/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/skater_time_on_ice_stats_now/position/RW/
```
---
<a name="team"></a>
## 3.Team  
<a name="team_all_season_summary"></a>
### 3.1 Get all season teams statistics summary(except for the current season)
- **Endpoint:** `/team_all_season_summary/`
- **Method:** GET
- **Description:** Retrieves aggregated statistics for all teams across all seasons they participated in the NHL.
- **Parameters:** No
- **Response:** JSON format
- **Schema table:**
  - **`team_name`** (string) - Full team name. The name of the NHL team.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`league`** (string) - The league in which the team played (e.g., NHL).
  - **`year_min`** (integer) - First year of NHL career.
  - **`year_max`** (integer) - Last year of NHL career.
  - **`years`** (integer) - Total number of years the team has spent in the NHL.
  - **`games`** (integer) - Games Played. Total number of games played by the team during the regular season (all season). (except current season).
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout (all season). (except current season).
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout (all season). (except current season).
  - **`ties`** (integer) - Ties. The number of games that ended with an equal score for both teams at the end of regulation time, resulting in no winner. (all season). (except current season).
  - **`losses_ot`** (integer) - Overtime/Shootout Losses. Total number of games lost by the team in overtime or shootout for all season (relevant from 2000 season onward).
  - **`points`** (integer) - Points. Total points accumulated by the team during the regular season. (except current season).
  - **`points_pct`** (number, decimal) - Points percentage (i.e., points divided by maximum points). Expressed as a decimal (e.g., 0.523) (except current season).
  - **`years_playoffs`** (integer) - Number of years team made the playoffs.
  - **`years_division_champion`** (integer) - Number of years team finished first (or tied for first) in the division.
  - **`years_conference_champion`** (integer) - Years team won the playoff conference championship. This begins in 1981-82.
  - **`years_league_champion`** (integer) - Years team won the league championship.
  - **`years_cup_champion`** (integer) - Years team won the Stanley Cup.

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/team_all_season_summary/
```
<a name="team_all_season_summary/team_abbrev/{team_abbrev}"></a>
### 3.2 Get all season teams statistics summary by specific team(except for the current season)
- **Endpoint:** `/team_all_season_summary/team_abbrev/{team_abbrev}`
- **Method:** GET
- **Description:** Retrieves aggregated statistics for all teams across all seasons they participated in the NHL.
- **Parameters:**
   - **`{team_abbrev}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`team_name`** (string) - Full team name. The name of the NHL team.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`league`** (string) - The league in which the team played (e.g., NHL).
  - **`year_min`** (integer) - First year of NHL career.
  - **`year_max`** (integer) - Last year of NHL career.
  - **`years`** (integer) - Total number of years the team has spent in the NHL.
  - **`games`** (integer) - Games Played. Total number of games played by the team during the regular season (all season). (except current season).
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout (all season). (except current season).
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout (all season). (except current season).
  - **`ties`** (integer) - Ties. The number of games that ended with an equal score for both teams at the end of regulation time, resulting in no winner. (all season). (except current season).
  - **`losses_ot`** (integer) - Overtime/Shootout Losses. Total number of games lost by the team in overtime or shootout for all season (relevant from 2000 season onward).
  - **`points`** (integer) - Points. Total points accumulated by the team during the regular season. (except current season).
  - **`points_pct`** (number, decimal) - Points percentage (i.e., points divided by maximum points). Expressed as a decimal (e.g., 0.523) (except current season).
  - **`years_playoffs`** (integer) - Number of years team made the playoffs.
  - **`years_division_champion`** (integer) - Number of years team finished first (or tied for first) in the division.
  - **`years_conference_champion`** (integer) - Years team won the playoff conference championship. This begins in 1981-82.
  - **`years_league_champion`** (integer) - Years team won the league championship.
  - **`years_cup_champion`** (integer) - Years team won the Stanley Cup.

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/team_all_season_summary/team_abbrev/TOR/
```
<a name="team_analytics_5_on_5_{year}"></a>
### 3.3 Get teams analytics 5 on 5 by year
> [!NOTE]
> **Data available since 2016-17 season** 
- **Endpoint:** `/team_analytics_5_on_5_{year}/`
- **Method:** GET
- **Description:** Table presents advanced statistics for NHL teams , focusing on 5-on-5 play for specific season.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank. The position of the team in the ranking based on their performance metrics.
  - **`team_name`** (string) - Team Name. The name of the NHL team.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`playoff`** (string) - Indicator if the team made the playoffs that season (e.g., 'Yes', 'No).
  - **`shot_pct_5on5`** (number, decimal) - Shooting Percentage 5-on-5. Reflects shooting efficiency. Expressed as a decimal (e.g., 7.3).
  - **`sv_pct_5on5`** (number, decimal) - Save percentage 5-on-5. Reflects a goaltenders ability to stop shots during 5-on-5 situations. Expressed as a decimal (e.g., 0.923).
  - **`pdo`** (number, decimal) - Shooting % + Save %. Reflects the combined efficiency of a team’s shooters and goaltenders during 5-on-5 play. Used as an indicator of puck luck. Expressed as a decimal (e.g., 99.7).
  - **`corsi_for_5on5`** (integer) - Corsi For 5-on-5. Reflects a team’s total shot attempt generation (including shots on goal, missed, and blocked shots) during 5-on-5 play.
  - **`corsi_against_5on5`** (integer) - Corsi Against 5-on-5. Reflects the total number of shot attempts (shots on goal, blocked shots, and missed shots) against a team during 5-on-5 play.
  - **`corsi_pct_5on5`** (number, decimal) - Corsi For Percentage 5-on-5. Above 50% means the team was controlling the puck more often than not with this player on the ice in this situation. Expressed as a decimal (e.g., 52.5).
  - **`fenwick_for_5on5`** (integer) - Fenwick For 5-on-5. Reflects the total number of unblocked shot attempts (shots on goal plus missed shots, excluding blocked shots) generated by a team during 5-on-5 play.
  - **`fenwick_against_5on5`** (integer) - Fenwick Against 5-on-5. Reflects the total number of unblocked shot attempts (shots on goal plus missed shots, excluding blocked shots) allowed by a team during 5-on-5 play.
  - **`fenwick_pct_5on5`** (number, decimal) - Fenwick For % at 5-on-5. Above 50% means the team was controlling the puck more often than not with this player on the ice in this situation. Expressed as a decimal (e.g., 50.6).
  - **`exp_on_goals_for`** (number, decimal) - 'Expected Goals For' given where shots came from, for and against, while this player was on the ice at even strength. It's based on where the shots are coming from, compared to the league-wide shooting percentage for that shot location. Expressed as a decimal (e.g., 164.7).
  - **`exp_on_goals_against`** (number, decimal) - 'Expected Goals Against' given where shots came from, for and against, while this player was on the ice at even strength. It's based on where the shots are coming from, compared to the league-wide shooting percentage for that shot location. Expressed as a decimal (e.g., 166.4).
  - **`actual_goals`** (integer) - Actual goals for 5-on-5. Reflects the total number of goals scored by a team during 5-on-5 play—counting only goals that actually went into the net during even-strength, non-special teams situations.
  - **`actual_goals_against`** (integer) - Actual goals against 5-on-5. Reflects the total number of goals allowed by a team during 5-on-5 play—counting only the goals scored by the opposition during even-strength, non-special teams situations.
  - **`actual_expected_diff`** (integer) - Actual goal differential minus expected goal differential. A positive differential would indicate a team is converting or stopping an inordinate amount of good chances compared to league average. A negative differential would indicate a team is getting more good chances, but not converting or is allowing more than league norms. Negative values are shown with a minus sign (e.g., -34), while positive values appear without any sign (e.g., 12).
  - **`sc_for`** (integer) - Scoring chances for. Scoring chances are all shot attempts from within a certain range from the net. Reflected the number of dangerous scoring opportunities created by a team or player.
  - **`sc_against`** (integer) - Scoring chances against.  Reflected the number of dangerous scoring opportunities allowed by a team or player.
  - **`sc_for_pct`** (number, decimal) - Percentage of scoring chances in this team's favor. Expressed as a decimal (e.g., 48.4).
  - **`hdsc_for`** (integer) - High-danger scoring chances for. High-danger chances include shot attempts from the 'slot' area and rebounds, approximately.
  - **`hdsc_against`** (integer) - High-danger scoring chances against. Reflected the number of the most dangerous (high-quality) scoring opportunities allowed by a team or player.
  - **`hdsc_for_pct`** (number, decimal) - Percentage of high-danger scoring chances in this team's favor. Expressed as a decimal (e.g., 49.7).
  - **`hdscgoal_for`** (integer) - High-danger scoring chances for that lead to goals.
  - **`hdsc_shot_pct`** (number, decimal) - Percentage of high-danger scoring chances that are converted to goals, for this team. Expressed as a decimal (e.g., 17.5).
  - **`hdscgoal_against`** (integer) - High-danger scoring chances against that lead to goals.
  - **`hdsc_opp_shot_pct`** (number, decimal) - Percentage of high-danger scoring chances that are converted to goals, for this team's opponents. Expressed as a decimal (e.g., 14.9).

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/team_analytics_5_on_5_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/team_analytics_5_on_5_now/
```
<a name="team_analytics_5_on_5_{year}/team_abbrev/{team_abbrev}"></a>
### 3.4 Get teams analytics 5 on 5 by year and specific team
> [!NOTE]
> **Data available since 2016-17 season** 
- **Endpoint:** `/team_analytics_5_on_5_{year}/team_abbrev/{team_abbrev}/`
- **Method:** GET
- **Description:** Table presents advanced statistics for NHL teams , focusing on 5-on-5 play of a specific team for specific season
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{team_abbrev}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank. The position of the team in the ranking based on their performance metrics.
  - **`team_name`** (string) - Team Name. The name of the NHL team.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`playoff`** (string) - Indicator if the team made the playoffs that season (e.g., 'Yes', 'No).
  - **`shot_pct_5on5`** (number, decimal) - Shooting Percentage 5-on-5. Reflects shooting efficiency. Expressed as a decimal (e.g., 7.3).
  - **`sv_pct_5on5`** (number, decimal) - Save percentage 5-on-5. Reflects a goaltenders ability to stop shots during 5-on-5 situations. Expressed as a decimal (e.g., 0.923).
  - **`pdo`** (number, decimal) - Shooting % + Save %. Reflects the combined efficiency of a team’s shooters and goaltenders during 5-on-5 play. Used as an indicator of puck luck. Expressed as a decimal (e.g., 99.7).
  - **`corsi_for_5on5`** (integer) - Corsi For 5-on-5. Reflects a team’s total shot attempt generation (including shots on goal, missed, and blocked shots) during 5-on-5 play.
  - **`corsi_against_5on5`** (integer) - Corsi Against 5-on-5. Reflects the total number of shot attempts (shots on goal, blocked shots, and missed shots) against a team during 5-on-5 play.
  - **`corsi_pct_5on5`** (number, decimal) - Corsi For Percentage 5-on-5. Above 50% means the team was controlling the puck more often than not with this player on the ice in this situation. Expressed as a decimal (e.g., 52.5).
  - **`fenwick_for_5on5`** (integer) - Fenwick For 5-on-5. Reflects the total number of unblocked shot attempts (shots on goal plus missed shots, excluding blocked shots) generated by a team during 5-on-5 play.
  - **`fenwick_against_5on5`** (integer) - Fenwick Against 5-on-5. Reflects the total number of unblocked shot attempts (shots on goal plus missed shots, excluding blocked shots) allowed by a team during 5-on-5 play.
  - **`fenwick_pct_5on5`** (number, decimal) - Fenwick For % at 5-on-5. Above 50% means the team was controlling the puck more often than not with this player on the ice in this situation. Expressed as a decimal (e.g., 50.6).
  - **`exp_on_goals_for`** (number, decimal) - 'Expected Goals For' given where shots came from, for and against, while this player was on the ice at even strength. It's based on where the shots are coming from, compared to the league-wide shooting percentage for that shot location. Expressed as a decimal (e.g., 164.7).
  - **`exp_on_goals_against`** (number, decimal) - 'Expected Goals Against' given where shots came from, for and against, while this player was on the ice at even strength. It's based on where the shots are coming from, compared to the league-wide shooting percentage for that shot location. Expressed as a decimal (e.g., 166.4).
  - **`actual_goals`** (integer) - Actual goals for 5-on-5. Reflects the total number of goals scored by a team during 5-on-5 play—counting only goals that actually went into the net during even-strength, non-special teams situations.
  - **`actual_goals_against`** (integer) - Actual goals against 5-on-5. Reflects the total number of goals allowed by a team during 5-on-5 play—counting only the goals scored by the opposition during even-strength, non-special teams situations.
  - **`actual_expected_diff`** (integer) - Actual goal differential minus expected goal differential. A positive differential would indicate a team is converting or stopping an inordinate amount of good chances compared to league average. A negative differential would indicate a team is getting more good chances, but not converting or is allowing more than league norms. Negative values are shown with a minus sign (e.g., -34), while positive values appear without any sign (e.g., 12).
  - **`sc_for`** (integer) - Scoring chances for. Scoring chances are all shot attempts from within a certain range from the net. Reflected the number of dangerous scoring opportunities created by a team or player.
  - **`sc_against`** (integer) - Scoring chances against.  Reflected the number of dangerous scoring opportunities allowed by a team or player.
  - **`sc_for_pct`** (number, decimal) - Percentage of scoring chances in this team's favor. Expressed as a decimal (e.g., 48.4).
  - **`hdsc_for`** (integer) - High-danger scoring chances for. High-danger chances include shot attempts from the 'slot' area and rebounds, approximately.
  - **`hdsc_against`** (integer) - High-danger scoring chances against. Reflected the number of the most dangerous (high-quality) scoring opportunities allowed by a team or player.
  - **`hdsc_for_pct`** (number, decimal) - Percentage of high-danger scoring chances in this team's favor. Expressed as a decimal (e.g., 49.7).
  - **`hdscgoal_for`** (integer) - High-danger scoring chances for that lead to goals.
  - **`hdsc_shot_pct`** (number, decimal) - Percentage of high-danger scoring chances that are converted to goals, for this team. Expressed as a decimal (e.g., 17.5).
  - **`hdscgoal_against`** (integer) - High-danger scoring chances against that lead to goals.
  - **`hdsc_opp_shot_pct`** (number, decimal) - Percentage of high-danger scoring chances that are converted to goals, for this team's opponents. Expressed as a decimal (e.g., 14.9).

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/team_analytics_5_on_5_20212022/team_abbrev/TOR/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/team_analytics_5_on_5_now/team_abbrev/TOR/
```
<a name="expanded_standings_{year}"></a>
### 3.5 Get expanded standings teams by year
- **Endpoint:** `/expanded_standings_{year}/`
- **Method:** GET
- **Description:** Table presents expanded statistics for NHL teams , focusing on W-L-T\O
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank. The position of the team in the ranking based on their performance metrics.
  - **`team_name`** (string) - Team Name. The name of the NHL team.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`overall`** (string) - Overall W-L-T/O record (e.g., '28-14-6').
  - **`overall_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "overall" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.646').
  - **`shootout`** (string) - Shootout W-L record (e.g., '4-3', '0-3').
  - **`shootout_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "shootout" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '1.333').
  - **`ot`** (string) - Overtime W-L record, not including shootouts (e.g., '2-1', '3-5').
  - **`ot_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "ot" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.667').
  - **`home`** (string) - W-L-T/O record in home games (e.g., '2-11-5', '11-14-0').
  - **`home_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "home" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.768').
  - **`road`** (string) - W-L-T/O record in road games (e.g., '12-11-5').
  - **`road_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "road" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.628').
  - **`eas`** (string) - W-L-T/O record versus Eastern Conference teams (e.g., '6-2-5'). The value may be absent if the team did not play in this group.
  - **`eas_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "eas" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.518'). The value may be missing if the "eas" variable is missing.
  - **`easd`** (string) - W-L-T/O record versus East Division teams (e.g., '6-2-5'). The value may be absent if the team did not play in this group. Only valid for 2020-21 season.
  - **`easd_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "easd" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.714'). The value may be missing if the "easd" variable is missing. Only valid for 2020-21 season.
  - **`wes`** (string) - W-L-T/O record versus Western Conference teams (e.g., '21-28-7'). The value may be absent if the team did not play in this group.
  - **`wes_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "wes" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.518'). The value may be missing if the "wes" variable is missing.
  - **`atl`** (string) - W-L-T/O record versus Atlantic Division teams (e.g., '21-28-7'). The value may be absent if the team did not play in this group.
  - **`atl_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "atl" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.518'). The value may be missing if the "atl" variable is missing.
  - **`nth`** (string) - W-L-T/O record versus North Division teams (e.g., '35-14-7'). The value may be absent if the team did not play in this group.
  - **`nth_tsi`** (number, decimal) -  TSI - team succes index. The higher the value, the better the performance. Reflects the "nth" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.322'). The value may be missing if the "nth" variable is missing.
  - **`wesd`** (string) - W-L-T/O record versus West Division teams (e.g., '21-28-7'). The value may be absent if the team did not play in this group.
  - **`wesd_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "wesd" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.467'). The value may be missing if the "wesd" variable is missing.
  - **`nea`** (string) - W-L-T/O record versus Northeast Division teams (e.g., '19-27-10'). The value may be absent if the team did not play in this group.
  - **`nea_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "nea" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.705'). The value may be missing if the "nea" variable is missing.
  - **`sea`** (string) - W-L-T/O record versus Southeast Division teams (e.g., '18-26-12'). The value may be absent if the team did not play in this group.
  - **`sea_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "sea" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.536'). The value may be missing if the "sea" variable is missing.c
  - **`nwe`** (string) - W-L-T/O record versus Northwest Division teams (e.g., '26-27-3'). The value may be absent if the team did not play in this group.
  - **`nwe_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "nwe" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "nwe" variable is missing.
  - **`met`** (string) - W-L-T/O record versus Metropolitan Division teams (e.g., '17-30-9'). The value may be absent if the team did not play in this group.
  - **`met_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "met" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "met" variable is missing.
  - **`cen`** (string) - W-L-T/O record versus Central Division teams (e.g., '17-30-9'). The value may be absent if the team did not play in this group.
  - **`cen_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "cen" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "cen" variable is missing.
  - **`pac`** (string) - W-L-T/O record versus Pacific Division teams (e.g., '17-30-9'). The value may be absent if the team did not play in this group.
  - **`pac_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "pac" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "pac" variable is missing.
  - **`one_goal`** (string) - W-L-T/O record in games decided by 1 or fewer goals (e.g., '17-30-9'). 
  - **`one_goal_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "one_goal" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455').
  - **`three_goal`** (string) - W-L-T/O record in games decided by 3 or more goals (e.g., '17-30-9'). 
  - **`three_goal_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "three_goal" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455').
  - **`sep`** (string) - W-L-T/O record in the month of September (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`sep_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "sep" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "sep" variable is missing.
  - **`oct`** (string) - W-L-T/O record in the month of October (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`oct_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "oct" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "oct" variable is missing.
  - **`nov`** (string) - W-L-T/O record in the month of November (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`nov_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "nov" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "nov" variable is missing.
  - **`dec`** (string) - W-L-T/O record in the month of December (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`dec_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "dec" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "dec" variable is missing.
  - **`jan`** (string) - W-L-T/O record in the month of January (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`jan_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "jan" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "jan" variable is missing.
  - **`feb`** (string) - W-L-T/O record in the month of February (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`feb_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "feb" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "feb" variable is missing.
  - **`mar`** (string) - W-L-T/O record in the month of March (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`mar_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "mar" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "mar" variable is missing.
  - **`apr`** (string) - W-L-T/O record in the month of April (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`apr_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "apr" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "apr" variable is missing.
  - **`may`** (string) - W-L-T/O record in the month of May (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`may_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "may" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "may" variable is missing.   

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/expanded_standings_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/expanded_standings_now/
```
<a name="expanded_standings_{year}/team_abbrev/{team_abbrev}"></a>
### 3.6 Get expanded standings teams by year and specific team
- **Endpoint:** `/expanded_standings_{year}/team_abbrev/{team_abbrev}`
- **Method:** GET
- **Description:** Table presents expanded statistics for NHL teams , focusing on W-L-T\O by specific team
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{team_abbrev}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank. The position of the team in the ranking based on their performance metrics.
  - **`team_name`** (string) - Team Name. The name of the NHL team.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`overall`** (string) - Overall W-L-T/O record (e.g., '28-14-6').
  - **`overall_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "overall" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.646').
  - **`shootout`** (string) - Shootout W-L record (e.g., '4-3', '0-3').
  - **`shootout_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "shootout" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '1.333').
  - **`ot`** (string) - Overtime W-L record, not including shootouts (e.g., '2-1', '3-5').
  - **`ot_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "ot" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.667').
  - **`home`** (string) - W-L-T/O record in home games (e.g., '2-11-5', '11-14-0').
  - **`home_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "home" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.768').
  - **`road`** (string) - W-L-T/O record in road games (e.g., '12-11-5').
  - **`road_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "road" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.628').
  - **`eas`** (string) - W-L-T/O record versus Eastern Conference teams (e.g., '6-2-5'). The value may be absent if the team did not play in this group.
  - **`eas_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "eas" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.518'). The value may be missing if the "eas" variable is missing.
  - **`easd`** (string) - W-L-T/O record versus East Division teams (e.g., '6-2-5'). The value may be absent if the team did not play in this group. Only valid for 2020-21 season.
  - **`easd_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "easd" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.714'). The value may be missing if the "easd" variable is missing. Only valid for 2020-21 season.
  - **`wes`** (string) - W-L-T/O record versus Western Conference teams (e.g., '21-28-7'). The value may be absent if the team did not play in this group.
  - **`wes_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "wes" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.518'). The value may be missing if the "wes" variable is missing.
  - **`atl`** (string) - W-L-T/O record versus Atlantic Division teams (e.g., '21-28-7'). The value may be absent if the team did not play in this group.
  - **`atl_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "atl" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.518'). The value may be missing if the "atl" variable is missing.
  - **`nth`** (string) - W-L-T/O record versus North Division teams (e.g., '35-14-7'). The value may be absent if the team did not play in this group.
  - **`nth_tsi`** (number, decimal) -  TSI - team succes index. The higher the value, the better the performance. Reflects the "nth" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.322'). The value may be missing if the "nth" variable is missing.
  - **`wesd`** (string) - W-L-T/O record versus West Division teams (e.g., '21-28-7'). The value may be absent if the team did not play in this group.
  - **`wesd_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "wesd" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.467'). The value may be missing if the "wesd" variable is missing.
  - **`nea`** (string) - W-L-T/O record versus Northeast Division teams (e.g., '19-27-10'). The value may be absent if the team did not play in this group.
  - **`nea_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "nea" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.705'). The value may be missing if the "nea" variable is missing.
  - **`sea`** (string) - W-L-T/O record versus Southeast Division teams (e.g., '18-26-12'). The value may be absent if the team did not play in this group.
  - **`sea_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "sea" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.536'). The value may be missing if the "sea" variable is missing.c
  - **`nwe`** (string) - W-L-T/O record versus Northwest Division teams (e.g., '26-27-3'). The value may be absent if the team did not play in this group.
  - **`nwe_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "nwe" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "nwe" variable is missing.
  - **`met`** (string) - W-L-T/O record versus Metropolitan Division teams (e.g., '17-30-9'). The value may be absent if the team did not play in this group.
  - **`met_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "met" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "met" variable is missing.
  - **`cen`** (string) - W-L-T/O record versus Central Division teams (e.g., '17-30-9'). The value may be absent if the team did not play in this group.
  - **`cen_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "cen" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "cen" variable is missing.
  - **`pac`** (string) - W-L-T/O record versus Pacific Division teams (e.g., '17-30-9'). The value may be absent if the team did not play in this group.
  - **`pac_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "pac" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "pac" variable is missing.
  - **`one_goal`** (string) - W-L-T/O record in games decided by 1 or fewer goals (e.g., '17-30-9'). 
  - **`one_goal_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "one_goal" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455').
  - **`three_goal`** (string) - W-L-T/O record in games decided by 3 or more goals (e.g., '17-30-9'). 
  - **`three_goal_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "three_goal" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455').
  - **`sep`** (string) - W-L-T/O record in the month of September (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`sep_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "sep" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "sep" variable is missing.
  - **`oct`** (string) - W-L-T/O record in the month of October (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`oct_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "oct" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "oct" variable is missing.
  - **`nov`** (string) - W-L-T/O record in the month of November (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`nov_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "nov" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "nov" variable is missing.
  - **`dec`** (string) - W-L-T/O record in the month of December (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`dec_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "dec" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "dec" variable is missing.
  - **`jan`** (string) - W-L-T/O record in the month of January (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`jan_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "jan" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "jan" variable is missing.
  - **`feb`** (string) - W-L-T/O record in the month of February (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`feb_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "feb" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "feb" variable is missing.
  - **`mar`** (string) - W-L-T/O record in the month of March (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`mar_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "mar" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "mar" variable is missing.
  - **`apr`** (string) - W-L-T/O record in the month of April (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`apr_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "apr" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "apr" variable is missing.
  - **`may`** (string) - W-L-T/O record in the month of May (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`may_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "may" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "may" variable is missing.   

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/expanded_standings_20212022/team_abbrev/MTL/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/expanded_standings_now/team_abbrev/MTL/
```
<a name="expanded_standings_{year}/rank/{rank}"></a>
### 3.7 Get expanded standings teams by year and specific rank
- **Endpoint:** `/expanded_standings_{year}/rank/{rank}`
- **Method:** GET
- **Description:** Table presents expanded statistics for NHL teams , focusing on W-L-T\O by specific rank
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{rank}`** (integer) - Rank. The position of the team in the ranking based on their performance metrics.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank. The position of the team in the ranking based on their performance metrics.
  - **`team_name`** (string) - Team Name. The name of the NHL team.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`overall`** (string) - Overall W-L-T/O record (e.g., '28-14-6').
  - **`overall_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "overall" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.646').
  - **`shootout`** (string) - Shootout W-L record (e.g., '4-3', '0-3').
  - **`shootout_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "shootout" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '1.333').
  - **`ot`** (string) - Overtime W-L record, not including shootouts (e.g., '2-1', '3-5').
  - **`ot_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "ot" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.667').
  - **`home`** (string) - W-L-T/O record in home games (e.g., '2-11-5', '11-14-0').
  - **`home_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "home" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.768').
  - **`road`** (string) - W-L-T/O record in road games (e.g., '12-11-5').
  - **`road_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "road" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.628').
  - **`eas`** (string) - W-L-T/O record versus Eastern Conference teams (e.g., '6-2-5'). The value may be absent if the team did not play in this group.
  - **`eas_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "eas" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.518'). The value may be missing if the "eas" variable is missing.
  - **`easd`** (string) - W-L-T/O record versus East Division teams (e.g., '6-2-5'). The value may be absent if the team did not play in this group. Only valid for 2020-21 season.
  - **`easd_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "easd" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.714'). The value may be missing if the "easd" variable is missing. Only valid for 2020-21 season.
  - **`wes`** (string) - W-L-T/O record versus Western Conference teams (e.g., '21-28-7'). The value may be absent if the team did not play in this group.
  - **`wes_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "wes" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.518'). The value may be missing if the "wes" variable is missing.
  - **`atl`** (string) - W-L-T/O record versus Atlantic Division teams (e.g., '21-28-7'). The value may be absent if the team did not play in this group.
  - **`atl_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "atl" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.518'). The value may be missing if the "atl" variable is missing.
  - **`nth`** (string) - W-L-T/O record versus North Division teams (e.g., '35-14-7'). The value may be absent if the team did not play in this group.
  - **`nth_tsi`** (number, decimal) -  TSI - team succes index. The higher the value, the better the performance. Reflects the "nth" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.322'). The value may be missing if the "nth" variable is missing.
  - **`wesd`** (string) - W-L-T/O record versus West Division teams (e.g., '21-28-7'). The value may be absent if the team did not play in this group.
  - **`wesd_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "wesd" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.467'). The value may be missing if the "wesd" variable is missing.
  - **`nea`** (string) - W-L-T/O record versus Northeast Division teams (e.g., '19-27-10'). The value may be absent if the team did not play in this group.
  - **`nea_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "nea" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.705'). The value may be missing if the "nea" variable is missing.
  - **`sea`** (string) - W-L-T/O record versus Southeast Division teams (e.g., '18-26-12'). The value may be absent if the team did not play in this group.
  - **`sea_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "sea" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.536'). The value may be missing if the "sea" variable is missing.c
  - **`nwe`** (string) - W-L-T/O record versus Northwest Division teams (e.g., '26-27-3'). The value may be absent if the team did not play in this group.
  - **`nwe_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "nwe" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "nwe" variable is missing.
  - **`met`** (string) - W-L-T/O record versus Metropolitan Division teams (e.g., '17-30-9'). The value may be absent if the team did not play in this group.
  - **`met_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "met" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "met" variable is missing.
  - **`cen`** (string) - W-L-T/O record versus Central Division teams (e.g., '17-30-9'). The value may be absent if the team did not play in this group.
  - **`cen_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "cen" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "cen" variable is missing.
  - **`pac`** (string) - W-L-T/O record versus Pacific Division teams (e.g., '17-30-9'). The value may be absent if the team did not play in this group.
  - **`pac_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "pac" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "pac" variable is missing.
  - **`one_goal`** (string) - W-L-T/O record in games decided by 1 or fewer goals (e.g., '17-30-9'). 
  - **`one_goal_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "one_goal" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455').
  - **`three_goal`** (string) - W-L-T/O record in games decided by 3 or more goals (e.g., '17-30-9'). 
  - **`three_goal_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "three_goal" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455').
  - **`sep`** (string) - W-L-T/O record in the month of September (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`sep_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "sep" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "sep" variable is missing.
  - **`oct`** (string) - W-L-T/O record in the month of October (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`oct_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "oct" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "oct" variable is missing.
  - **`nov`** (string) - W-L-T/O record in the month of November (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`nov_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "nov" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "nov" variable is missing.
  - **`dec`** (string) - W-L-T/O record in the month of December (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`dec_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "dec" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "dec" variable is missing.
  - **`jan`** (string) - W-L-T/O record in the month of January (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`jan_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "jan" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "jan" variable is missing.
  - **`feb`** (string) - W-L-T/O record in the month of February (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`feb_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "feb" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "feb" variable is missing.
  - **`mar`** (string) - W-L-T/O record in the month of March (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`mar_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "mar" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "mar" variable is missing.
  - **`apr`** (string) - W-L-T/O record in the month of April (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`apr_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "apr" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "apr" variable is missing.
  - **`may`** (string) - W-L-T/O record in the month of May (e.g., '17-30-9'). The value may be absent if the team did not play in this month.
  - **`may_tsi`** (number, decimal) - TSI - team succes index. The higher the value, the better the performance. Reflects the "may" variable as a number, reflects the team's success in this indicator. Expressed as a decimal (e.g., '0.455'). The value may be missing if the "may" variable is missing.   

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/expanded_standings_20212022/rank/3/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/expanded_standings_now/rank/3/
```
<a name="team_vs_team_{year}"></a>
### 3.8 Get team versus team by year
- **Endpoint:** `/team_vs_team_{year}`
- **Method:** GET
- **Description:**  This table provides detailed NHL team statistics against each opponent for a specific season. For every head-to-head matchup, the W-L-T/O record and a Team Success Index (TSI) are shown.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`team_name`** (string) - Team Name. The name of the NHL team.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
For each NHL team-opponent pair (e.g., "ANA", "ARI", "ATL", etc.), there are two columns:
  - **`XXX`** (string) - W-L-T/O record versus team XXX (for example: '3-2-0' means 3 wins, 2 losses, 0 ties/overtime losses). The column is omitted if the opponent team did not participate in the given season.
  - **`XXX_tsi`** (number, decimal) - TSI — team success index versus team XXX. The higher the value, the better the performance against this opponent. Expressed as a decimal (e.g., 0.382). The value may be missing if the "XXX" column is missing.  
**List of possible opponent columns (XXX):**  
ANA, ARI, ATL, BOS, BUF, CAR, CBJ, CGY, CHI, COL, DAL, DET, EDM, FLA, LAK, MDA, MIN, MTL, NJD, NSH, NYI, NYR, OTT, PHI, PHX, PIT, SJS, STL, SEA, TBL, TOR, UTA, VAN, VEG, WPG, WSH  
  For each opponent, there is a pair of columns: <team_abbrev>, <team_abbrev>_tsi.  
> [!NOTE]
> **If a particular team did not participate in the season, the related columns (e.g., "ATL", "ATL_tsi", "SEA", "SEA_tsi", etc.) will not be present in the table for that year.**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/team_vs_team_20132014/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/team_vs_team_now/
```
<a name="team_vs_team_{year}/{team_abbrev}"></a>
### 3.9 Get team versus team by year and specific team
- **Endpoint:** `/team_vs_team_{year}/{team_abbrev}`
- **Method:** GET
- **Description:**  This table provides detailed NHL team statistics against each opponent for a specific season. For every head-to-head matchup, the W-L-T/O record and a Team Success Index (TSI) are shown.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{team_abbrev}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`team_name`** (string) - Team Name. The name of the NHL team.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
For each NHL team-opponent pair (e.g., "ANA", "ARI", "ATL", etc.), there are two columns:
  - **`XXX`** (string) - W-L-T/O record versus team XXX (for example: '3-2-0' means 3 wins, 2 losses, 0 ties/overtime losses). The column is omitted if the opponent team did not participate in the given season.
  - **`XXX_tsi`** (number, decimal) - TSI — team success index versus team XXX. The higher the value, the better the performance against this opponent. Expressed as a decimal (e.g., 0.382). The value may be missing if the "XXX" column is missing.  
**List of possible opponent columns (XXX):**  
ANA, ARI, ATL, BOS, BUF, CAR, CBJ, CGY, CHI, COL, DAL, DET, EDM, FLA, LAK, MDA, MIN, MTL, NJD, NSH, NYI, NYR, OTT, PHI, PHX, PIT, SJS, STL, SEA, TBL, TOR, UTA, VAN, VEG, WPG, WSH  
  For each opponent, there is a pair of columns: <team_abbrev>, <team_abbrev>_tsi.  
> [!NOTE]
> **If a particular team did not participate in the season, the related columns (e.g., "ATL", "ATL_tsi", "SEA", "SEA_tsi", etc.) will not be present in the table for that year.**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/team_vs_team_20132014/MTL/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/team_vs_team_now/MTL/
```
<a name="roster_team_{year}"></a>
### 3.10 Get roster team by year
- **Endpoint:** `/roster_team_{year}`
- **Method:** GET
- **Description:**  Returns a consolidated roster table for all NHL teams for the specified season. For each player, core biographical and playing attributes, team, and experience are provided.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`number`** (string) - Sweater Number.
For each NHL team-opponent pair (e.g., "ANA", "ARI", "ATL", etc.), there are two columns:
  - **`player`** (string) - Full player name.
  - **`player_id `** (string) - Unique player identifier.
  - **`country_of_birth`** (string) - Country of birth (US, SE, CA, RU).
  - **`position`** (string) - Playing position ("F", "D", "G").
  - **`age`** (integer) - Age at/for the season.
  - **`height`** (string) - Height.
  - **`weight`** (string) - Weight.
  - **`shoots_and_catches`** (string) - Shooting/Catching side: skaters — "L"/"R" (Shoots); goalies — "L"/"R" (Catches).
  - **`years_experience`** (string) - Years experience in league (prior to this season).
  - **`birth_date`** (string) - Date of birth (January 19, 2004).

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/roster_team_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/roster_team_now/
```
<a name="roster_team_{year}/team_abbrev/{team_abbrev}"></a>
### 3.11 Get roster team by year and specific team
- **Endpoint:** `/roster_team_{year}/team_abbrev/{team_abbrev}/`
- **Method:** GET
- **Description:**  Returns the roster of the specified team for the given season with all attributes..
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{team_abbrev}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`number`** (string) - Sweater Number.
For each NHL team-opponent pair (e.g., "ANA", "ARI", "ATL", etc.), there are two columns:
  - **`player`** (string) - Full player name.
  - **`player_id `** (string) - Unique player identifier.
  - **`country_of_birth`** (string) - Country of birth (US, SE, CA, RU).
  - **`position`** (string) - Playing position ("F", "D", "G").
  - **`age`** (integer) - Age at/for the season.
  - **`height`** (string) - Height.
  - **`weight`** (string) - Weight.
  - **`shoots_and_catches`** (string) - Shooting/Catching side: skaters — "L"/"R" (Shoots); goalies — "L"/"R" (Catches).
  - **`years_experience`** (string) - Years experience in league (prior to this season).
  - **`birth_date`** (string) - Date of birth (January 19, 2004).

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/roster_team_20212022/team_abbrev/MTL/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/roster_team_now/team_abbrev/MTL/
```
<a name="roster_team_{year}/player_id/{player_id}"></a>
### 3.12 Get roster team by year and player ID
- **Endpoint:** `/roster_team_{year}/player_id/{player_id}/`
- **Method:** GET
- **Description:** Returns row(s) for the specified player in the given season by unique player ID. Useful to retrieve the player’s season team assignment and attributes.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{player_id}`** (string) - Unique player identifier.
- **Response:** JSON format
- **Schema table:**
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`number`** (string) - Sweater Number.
For each NHL team-opponent pair (e.g., "ANA", "ARI", "ATL", etc.), there are two columns:
  - **`player`** (string) - Full player name.
  - **`player_id `** (string) - Unique player identifier.
  - **`country_of_birth`** (string) - Country of birth (US, SE, CA, RU).
  - **`position`** (string) - Playing position ("F", "D", "G").
  - **`age`** (integer) - Age at/for the season.
  - **`height`** (string) - Height.
  - **`weight`** (string) - Weight.
  - **`shoots_and_catches`** (string) - Shooting/Catching side: skaters — "L"/"R" (Shoots); goalies — "L"/"R" (Catches).
  - **`years_experience`** (string) - Years experience in league (prior to this season).
  - **`birth_date`** (string) - Date of birth (January 19, 2004).

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/roster_team_20212022/player_id/grantde01/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/roster_team_now/player_id/grantde01/
```
<a name="roster_team_{year}/position/{position}"></a>
### 3.13 Get roster team by year and position
- **Endpoint:** `/roster_team_{year}/position/{position}/`
- **Method:** GET
- **Description:** Returns the roster for all teams in the specified season, filtered by position.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{position}`** (string) - Playing position ("F", "D", "G").
- **Response:** JSON format
- **Schema table:**
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`number`** (string) - Sweater Number.
  - **`player`** (string) - Full player name.
  - **`player_id `** (string) - Unique player identifier.
  - **`country_of_birth`** (string) - Country of birth (US, SE, CA, RU).
  - **`position`** (string) - Playing position ("F", "D", "G").
  - **`age`** (integer) - Age at/for the season.
  - **`height`** (string) - Height.
  - **`weight`** (string) - Weight.
  - **`shoots_and_catches`** (string) - Shooting/Catching side: skaters — "L"/"R" (Shoots); goalies — "L"/"R" (Catches).
  - **`years_experience`** (string) - Years experience in league (prior to this season).
  - **`birth_date`** (string) - Date of birth (January 19, 2004).

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/roster_team_20212022/position/G/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/roster_team_now/position/G/
```
<a name="injuries_now"></a>
### 3.14 Get injuries team now
- **Endpoint:** `/injuries_now/`
- **Method:** GET
- **Description:** Returns the injuries team, all team.
- **Parameters:** No
- **Response:** JSON format
- **Schema table:**
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`number`** (string) - Sweater Number.
  - **`player`** (string) - Full player name.
  - **`player_id `** (string) - Unique player identifier.
  - **`date_injury`** (string) - Date injury (Wed, Aug 28, 2024).
  - **`date_injury_iso`** (string) - Date injury YYYY-MM-DD (2024-08-28).
  - **`injury_type`** (string) - Type of injury
  - **`injury_note`** (string) - Explanation of the player's injury, how long he will miss and whether he will play.

##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/injuries_now/
```
<a name="injuries_now/team_abbrev/{team_abbrev}"></a>
### 3.15 Get injuries team now by specific team
- **Endpoint:** `/injuries_now/team_abbrev/{team_abbrev}/`
- **Method:** GET
- **Description:** Returns the injuries team,  filtered by team.
- **Parameters:**
   - **`{team_abbrev}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`number`** (string) - Sweater Number.
  - **`player`** (string) - Full player name.
  - **`player_id `** (string) - Unique player identifier.
  - **`date_injury`** (string) - Date injury (Wed, Aug 28, 2024).
  - **`date_injury_iso`** (string) - Date injury YYYY-MM-DD (2024-08-28).
  - **`injury_type`** (string) - Type of injury
  - **`injury_note`** (string) - Explanation of the player's injury, how long he will miss and whether he will play.

##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/injuries_now/team_abbrev/PHI/
```
<a name="injuries_now/player_id/{player_id}"></a>
### 3.16 Get injuries team now by player ID
- **Endpoint:** `/injuries_now/player_id/{player_id}/`
- **Method:** GET
- **Description:** Returns the injuries team,  filtered by player ID.
- **Parameters:**
   - **`{player_id}`** (string) - Unique player identifier.
- **Response:** JSON format
- **Schema table:**
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`number`** (string) - Sweater Number.
  - **`player`** (string) - Full player name.
  - **`player_id `** (string) - Unique player identifier.
  - **`date_injury`** (string) - Date injury (Wed, Aug 28, 2024).
  - **`date_injury_iso`** (string) - Date injury YYYY-MM-DD (2024-08-28).
  - **`injury_type`** (string) - Type of injury
  - **`injury_note`** (string) - Explanation of the player's injury, how long he will miss and whether he will play.

##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/injuries_now/player_id/ellisry01/
```
<a name="scoring_by_period_{year}"></a>
### 3.17 Get scoring (period) by year
- **Endpoint:** `/scoring_by_period_{year}/`
- **Method:** GET
- **Description:** Returns goals by period in the given season. Values are split into Team and Opponent and grouped by Overall/Home/Away with period breakdown 1/2/3/OT/Total.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`scoring_overall_1_period_team`** (integer) - Team goals in 1st period across all games (overall).
  - **`scoring_overall_2_period_team`** (integer) - Team goals in 2nd period across all games (overall).
  - **`scoring_overall_3_period_team`** (integer) - Team goals in 3rd period across all games (overall).
  - **`scoring_overall_ot_team`** (integer) - Team goals in overtime across all games (overall).
  - **`scoring_overall_total_team`** (integer) - Team total goals across all games (overall).
  - **`scoring_overall_1_period_opponent`** (integer) - Opponent goals in 1st period across all games (overall).
  - **`scoring_overall_2_period_opponent`** (integer) - Opponent goals in 2nd period across all games (overall).
  - **`scoring_overall_3_period_opponent`** (integer) - Opponent goals in 3rd period across all games (overall).
  - **`scoring_overall_ot_opponent`** (integer) - Opponent goals in overtime across all games (overall).
  - **`scoring_overall_total_opponent`** (integer) - Opponent total goals across all games (overall).
  - **`scoring_home_1_period_team `** (integer) - Team goals in 1st period in home games.
  - **`scoring_home_2_period_team `** (integer) - Team goals in 2nd period in home games.
  - **`scoring_home_3_period_team `** (integer) - Team goals in 2rd period in home games.
  - **`scoring_home_ot_team`** (integer) - Team goals in overtime in home games.
  - **`scoring_home_total_team`** (integer) - Team total goals in home games.
  - **`scoring_home_1_period_opponent`** (integer) - Opponent goals in 1st period in the team’s home games.
  - **`scoring_home_2_period_opponent`** (integer) - Opponent goals in 2nd period in the team’s home games.
  - **`scoring_home_3_period_opponent`** (integer) - Opponent goals in 3rd period in the team’s home games.
  - **`scoring_home_ot_opponent`** (integer) - Opponent goals in overtime in the team’s home games.
  - **`scoring_home_total_opponent`** (integer) - Opponent total goals in the team’s home games.
  - **`scoring_away_1_period_team `** (integer) - Team goals in 1st period in away games.
  - **`scoring_away_2_period_team `** (integer) - Team goals in 2nd period in away games.
  - **`scoring_away_3_period_team `** (integer) - Team goals in 2rd period in away games.
  - **`scoring_away_ot_team`** (integer) - Team goals in overtime in away games.
  - **`scoring_away_total_team`** (integer) - Team total goals in away games.
  - **`scoring_away_1_period_opponent`** (integer) - Opponent goals in 1st period when the team plays away.
  - **`scoring_away_2_period_opponent`** (integer) - Opponent goals in 2nd period when the team plays away.
  - **`scoring_away_3_period_opponent`** (integer) - Opponent goals in 3rd period when the team plays away.
  - **`scoring_away_ot_opponent`** (integer) - Opponent goals in overtime when the team plays away.
  - **`scoring_away_total_opponent`** (integer) - Opponent total goals when the team plays away.

> [!NOTE]
> **Data starts with the 2014-15 season**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/scoring_by_period_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/scoring_by_period_now/
```
<a name="scoring_by_period_{year}/team_abbrev/{team_abbrev}"></a>
### 3.18 Get scoring (period) by year and specific team
- **Endpoint:** `/scoring_by_period_{year}/team_abbrev/{team_abbrev}/`
- **Method:** GET
- **Description:** Returns goals by period for the specified team in the given season. Values are split into Team and Opponent and grouped by Overall/Home/Away with period breakdown 1/2/3/OT/Total.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{team_abbrev}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`scoring_overall_1_period_team`** (integer) - Team goals in 1st period across all games (overall).
  - **`scoring_overall_2_period_team`** (integer) - Team goals in 2nd period across all games (overall).
  - **`scoring_overall_3_period_team`** (integer) - Team goals in 3rd period across all games (overall).
  - **`scoring_overall_ot_team`** (integer) - Team goals in overtime across all games (overall).
  - **`scoring_overall_total_team`** (integer) - Team total goals across all games (overall).
  - **`scoring_overall_1_period_opponent`** (integer) - Opponent goals in 1st period across all games (overall).
  - **`scoring_overall_2_period_opponent`** (integer) - Opponent goals in 2nd period across all games (overall).
  - **`scoring_overall_3_period_opponent`** (integer) - Opponent goals in 3rd period across all games (overall).
  - **`scoring_overall_ot_opponent`** (integer) - Opponent goals in overtime across all games (overall).
  - **`scoring_overall_total_opponent`** (integer) - Opponent total goals across all games (overall).
  - **`scoring_home_1_period_team `** (integer) - Team goals in 1st period in home games.
  - **`scoring_home_2_period_team `** (integer) - Team goals in 2nd period in home games.
  - **`scoring_home_3_period_team `** (integer) - Team goals in 2rd period in home games.
  - **`scoring_home_ot_team`** (integer) - Team goals in overtime in home games.
  - **`scoring_home_total_team`** (integer) - Team total goals in home games.
  - **`scoring_home_1_period_opponent`** (integer) - Opponent goals in 1st period in the team’s home games.
  - **`scoring_home_2_period_opponent`** (integer) - Opponent goals in 2nd period in the team’s home games.
  - **`scoring_home_3_period_opponent`** (integer) - Opponent goals in 3rd period in the team’s home games.
  - **`scoring_home_ot_opponent`** (integer) - Opponent goals in overtime in the team’s home games.
  - **`scoring_home_total_opponent`** (integer) - Opponent total goals in the team’s home games.
  - **`scoring_away_1_period_team `** (integer) - Team goals in 1st period in away games.
  - **`scoring_away_2_period_team `** (integer) - Team goals in 2nd period in away games.
  - **`scoring_away_3_period_team `** (integer) - Team goals in 2rd period in away games.
  - **`scoring_away_ot_team`** (integer) - Team goals in overtime in away games.
  - **`scoring_away_total_team`** (integer) - Team total goals in away games.
  - **`scoring_away_1_period_opponent`** (integer) - Opponent goals in 1st period when the team plays away.
  - **`scoring_away_2_period_opponent`** (integer) - Opponent goals in 2nd period when the team plays away.
  - **`scoring_away_3_period_opponent`** (integer) - Opponent goals in 3rd period when the team plays away.
  - **`scoring_away_ot_opponent`** (integer) - Opponent goals in overtime when the team plays away.
  - **`scoring_away_total_opponent`** (integer) - Opponent total goals when the team plays away.

> [!NOTE]
> **Data starts with the 2014-15 season**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/scoring_by_period_20212022/team_abbrev/MTL/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/scoring_by_period_now/team_abbrev/MTL/
```
<a name="shots_by_period_{year}"></a>
### 3.19 Get shots (period) by year
- **Endpoint:** `/shots_by_period_{year}/`
- **Method:** GET
- **Description:** Returns shots by period in the given season. Values are split into Team and Opponent and grouped by Overall/Home/Away with period breakdown 1/2/3/OT/Total.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`shots_overall_1_period_team`** (integer) - Team goals in 1st period across all games (overall).
  - **`shots_overall_2_period_team`** (integer) - Team goals in 2nd period across all games (overall).
  - **`shots_overall_3_period_team`** (integer) - Team goals in 3rd period across all games (overall).
  - **`shots_overall_ot_team`** (integer) - Team goals in overtime across all games (overall).
  - **`shots_overall_total_team`** (integer) - Team total goals across all games (overall).
  - **`shots_overall_1_period_opponent`** (integer) - Opponent goals in 1st period across all games (overall).
  - **`shots_overall_2_period_opponent`** (integer) - Opponent goals in 2nd period across all games (overall).
  - **`shots_overall_3_period_opponent`** (integer) - Opponent goals in 3rd period across all games (overall).
  - **`shots_overall_ot_opponent`** (integer) - Opponent goals in overtime across all games (overall).
  - **`shots_overall_total_opponent`** (integer) - Opponent total goals across all games (overall).
  - **`shots_home_1_period_team `** (integer) - Team goals in 1st period in home games.
  - **`shots_home_2_period_team `** (integer) - Team goals in 2nd period in home games.
  - **`shots_home_3_period_team `** (integer) - Team goals in 2rd period in home games.
  - **`shots_home_ot_team`** (integer) - Team goals in overtime in home games.
  - **`shots_home_total_team`** (integer) - Team total goals in home games.
  - **`shots_home_1_period_opponent`** (integer) - Opponent goals in 1st period in the team’s home games.
  - **`shots_home_2_period_opponent`** (integer) - Opponent goals in 2nd period in the team’s home games.
  - **`shots_home_3_period_opponent`** (integer) - Opponent goals in 3rd period in the team’s home games.
  - **`shots_home_ot_opponent`** (integer) - Opponent goals in overtime in the team’s home games.
  - **`shots_home_total_opponent`** (integer) - Opponent total goals in the team’s home games.
  - **`shots_away_1_period_team `** (integer) - Team goals in 1st period in away games.
  - **`shots_away_2_period_team `** (integer) - Team goals in 2nd period in away games.
  - **`shots_away_3_period_team `** (integer) - Team goals in 2rd period in away games.
  - **`shots_away_ot_team`** (integer) - Team goals in overtime in away games.
  - **`shots_away_total_team`** (integer) - Team total goals in away games.
  - **`shots_away_1_period_opponent`** (integer) - Opponent goals in 1st period when the team plays away.
  - **`shots_away_2_period_opponent`** (integer) - Opponent goals in 2nd period when the team plays away.
  - **`shots_away_3_period_opponent`** (integer) - Opponent goals in 3rd period when the team plays away.
  - **`shots_away_ot_opponent`** (integer) - Opponent goals in overtime when the team plays away.
  - **`shots_away_total_opponent`** (integer) - Opponent total goals when the team plays away.

> [!NOTE]
> **Data starts with the 2014-15 season**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/shots_by_period_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/shots_by_period_now/
```
<a name="shots_by_period_{year}/team_abbrev/{team_abbrev}"></a>
### 3.20 Get shots (period) by year and specific team
- **Endpoint:** `/shots_by_period_{year}/team_abbrev/{team_abbrev}/`
- **Method:** GET
- **Description:** Returns shots by period for the specified team in the given season. Values are split into Team and Opponent and grouped by Overall/Home/Away with period breakdown 1/2/3/OT/Total.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{team_abbrev}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`shots_overall_1_period_team`** (integer) - Team goals in 1st period across all games (overall).
  - **`shots_overall_2_period_team`** (integer) - Team goals in 2nd period across all games (overall).
  - **`shots_overall_3_period_team`** (integer) - Team goals in 3rd period across all games (overall).
  - **`shots_overall_ot_team`** (integer) - Team goals in overtime across all games (overall).
  - **`shots_overall_total_team`** (integer) - Team total goals across all games (overall).
  - **`shots_overall_1_period_opponent`** (integer) - Opponent goals in 1st period across all games (overall).
  - **`shots_overall_2_period_opponent`** (integer) - Opponent goals in 2nd period across all games (overall).
  - **`shots_overall_3_period_opponent`** (integer) - Opponent goals in 3rd period across all games (overall).
  - **`shots_overall_ot_opponent`** (integer) - Opponent goals in overtime across all games (overall).
  - **`shots_overall_total_opponent`** (integer) - Opponent total goals across all games (overall).
  - **`shots_home_1_period_team `** (integer) - Team goals in 1st period in home games.
  - **`shots_home_2_period_team `** (integer) - Team goals in 2nd period in home games.
  - **`shots_home_3_period_team `** (integer) - Team goals in 2rd period in home games.
  - **`shots_home_ot_team`** (integer) - Team goals in overtime in home games.
  - **`shots_home_total_team`** (integer) - Team total goals in home games.
  - **`shots_home_1_period_opponent`** (integer) - Opponent goals in 1st period in the team’s home games.
  - **`shots_home_2_period_opponent`** (integer) - Opponent goals in 2nd period in the team’s home games.
  - **`shots_home_3_period_opponent`** (integer) - Opponent goals in 3rd period in the team’s home games.
  - **`shots_home_ot_opponent`** (integer) - Opponent goals in overtime in the team’s home games.
  - **`shots_home_total_opponent`** (integer) - Opponent total goals in the team’s home games.
  - **`shots_away_1_period_team `** (integer) - Team goals in 1st period in away games.
  - **`shots_away_2_period_team `** (integer) - Team goals in 2nd period in away games.
  - **`shots_away_3_period_team `** (integer) - Team goals in 2rd period in away games.
  - **`shots_away_ot_team`** (integer) - Team goals in overtime in away games.
  - **`shots_away_total_team`** (integer) - Team total goals in away games.
  - **`shots_away_1_period_opponent`** (integer) - Opponent goals in 1st period when the team plays away.
  - **`shots_away_2_period_opponent`** (integer) - Opponent goals in 2nd period when the team plays away.
  - **`shots_away_3_period_opponent`** (integer) - Opponent goals in 3rd period when the team plays away.
  - **`shots_away_ot_opponent`** (integer) - Opponent goals in overtime when the team plays away.
  - **`shots_away_total_opponent`** (integer) - Opponent total goals when the team plays away.

> [!NOTE]
> **Data starts with the 2014-15 season**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/shots_by_period_20212022/team_abbrev/MTL/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/shots_by_period_now/team_abbrev/MTL/
```
<a name="records_team_{year}"></a>
### 3.21 Get miscellaneous records teams by year
- **Endpoint:** `/records_team_{year}/`
- **Method:** GET
- **Description:** Returns team miscellaneous situational records for the given season. For each team, provides Overall/Home/Away splits across several situations (e.g., scoring first, opponent scoring first, outshooting/outshot, one-goal games, and when leading/trailing/tied after periods). Each record is returned as a W-L-OT string plus a computed Team Points Percentage index (_tsi), where points percentage is calculated as (2*W + 1*OT) / (2*(W+L+OT)), rounded to 4 decimals.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`overall_scoring_first`** (string) - Record (W-L-OT) when the team scores first, all games.
  - **`overall_scoring_first_tsi`** (number, decimal) - Points percentage when scoring first; higher is better.
  - **`overall_opponent_scores_first`** (string) - Record (W-L-OT) when the opponent scores first, all games.
  - **`overall_opponent_scores_first_tsi`** (number, decimal) - Points percentage when conceding first; higher is better within this negative context (resilience).
  - **`overall_when_outshooting_opponent`** (string) - Record (W-L-OT) when outshooting the opponent, all games.
  - **`overall_when_outshooting_opponent_tsi`** (number, decimal) - Points percentage when outshooting the opponent; higher is better.
  - **`overall_when_outshot_opponent`** (string) - Record (W-L-OT) when being outshot by the opponent, all games.
  - **`overall_when_outshot_opponent_tsi`** (number, decimal) - Points percentage when outshot; higher is better within this negative context (withstanding pressure).
  - **`overall_1_goal_games`** (string) - Record (W-L-OT) in one-goal games, all games.
  - **`overall_1_goal_games_tsi`** (number, decimal) - Points percentage in one-goal games; higher is better.
  - **`overall_lead_after_1_period`** (string) - Record (W-L-OT) when leading after 1st period, all games.
  - **`overall_lead_after_1_period_tsi`** (number, decimal) - Points percentage when leading after 1st period; higher is better (closing out from early lead).
  - **`overall_trail_after_1_period`** (string) - Record (W-L-OT) when trailing after 1st period, all games.
  - **`overall_trail_after_1_period_tsi`** (number, decimal) - Points percentage when trailing after 1st period; higher is better within this negative context (comeback ability).
  - **`overall_tie_after_1_period`** (string) - Record (W-L-OT) when tied after 1st period, all games.
  - **`overall_tie_after_1_period_tsi`** (number, decimal) - Points percentage when tied after 1st period; higher is better.
  - **`overall_lead_after_2_periods`** (string) - Record (W-L-OT) when leading after 2nd period, all games.
  - **`overall_lead_after_2_periods_tsi`** (number, decimal) - Points percentage when leading after 2nd period; higher is better (finish ability).
  - **`overall_trail_after_2_periods`** (string) - Record (W-L-OT) when trailing after 2nd period, all games.
  - **`overall_trail_after_2_periods_tsi`** (number, decimal) - Points percentage when trailing after 2nd period; higher is better within this negative context (late resilience).
  - **`overall_tie_after_2_periods`** (string) - Record (W-L-OT) when tied after 2nd period, all games.
  - **`overall_tie_after_2_periods_tsi`** (number, decimal) - Points percentage when tied after 2nd period; higher is better.
  - **`home_scoring_first`** (string) - Record (W-L-OT) when the team scores first, home games.
  - **`home_scoring_first_tsi `** (number, decimal) - Points percentage when scoring first at home; higher is better.
  - **`home_opponent_scores_first`** (string) - Record (W-L-OT) when the opponent scores first, home games.
  - **`home_opponent_scores_first_tsi`** (number, decimal) - Points percentage when conceding first at home; higher is better within this negative context.
  - **`home_when_outshooting_opponent`** (string) - Record (W-L-OT) when outshooting the opponent, home games.
  - **`home_when_outshooting_opponent_tsi`** (number, decimal) - Points percentage when outshooting at home; higher is better.
  - **`home_when_outshot_opponent`** (string) - Record (W-L-OT) when being outshot by the opponent, home games.
  - **`home_when_outshot_opponent_tsi`** (number, decimal) - Points percentage when outshot at home; higher is better within this negative context.
  - **`home_1_goal_games`** (string) - Record (W-L-OT) in one-goal games, home games.
  - **`home_1_goal_games_tsi`** (number, decimal) - Points percentage in one-goal games at home; higher is better.
  - **`home_lead_after_1_period`** (string) - Record (W-L-OT) when leading after 1st period, home games.
  - **`home_lead_after_1_period_tsi`** (number, decimal) - Points percentage when leading after 1st period at home; higher is better.
  - **`home_trail_after_1_period`** (string) - Record (W-L-OT) when trailing after 1st period, home games.
  - **`home_trail_after_1_period_tsi`** (number, decimal) - Points percentage when trailing after 1st period at home; higher is better within this negative context.
  - **`home_tie_after_1_period`** (string) - Record (W-L-OT) when tied after 1st period, home games.
  - **`home_tie_after_1_period_tsi`** (number, decimal) - Points percentage when tied after 1st period at home; higher is better.
  - **`home_lead_after_2_periods`** (string) - Record (W-L-OT) when leading after 2nd period, home games.
  - **`home_lead_after_2_periods_tsi`** (number, decimal) - Points percentage when leading after 2nd period at home; higher is better.
  - **`home_trail_after_2_periods`** (string) - Record (W-L-OT) when trailing after 2nd period, home games.
  - **`home_trail_after_2_periods_tsi`** (number, decimal) - Points percentage when trailing after 2nd period at home; higher is better within this negative context.
  - **`home_tie_after_2_periods`** (string) - Record (W-L-OT) when tied after 2nd period, home games.
  - **`home_tie_after_2_periods_tsi`** (number, decimal) - Points percentage when tied after 2nd period at home; higher is better.
  - **`away_scoring_first`** (string) - Record (W-L-OT) when the team scores first, away games.
  - **`away_scoring_first_tsi`** (number, decimal) - Points percentage when scoring first away; higher is better.
  - **`away_opponent_scores_first`** (string) - Record (W-L-OT) when the opponent scores first, away games.
  - **`away_opponent_scores_first_tsi`** (number, decimal) - Points percentage when conceding first away; higher is better within this negative context.
  - **`away_when_outshooting_opponent`** (string) - Record (W-L-OT) when outshooting the opponent, away games.
  - **`away_when_outshooting_opponent_tsi`** (number, decimal) - Points percentage when outshooting away; higher is better.
  - **`away_when_outshot_opponent`** (string) - Record (W-L-OT) when being outshot by the opponent, away games.
  - **`away_when_outshot_opponent_tsi`** (number, decimal) - Points percentage when outshot away; higher is better within this negative context.
  - **`away_1_goal_games`** (string) - Record (W-L-OT) in one-goal games, away games.
  - **`away_1_goal_games_tsi`** (number, decimal) - Points percentage in one-goal games away; higher is better.
  - **`away_lead_after_1_period`** (string) - Record (W-L-OT) when leading after 1st period, away games.
  - **`away_lead_after_1_period_tsi`** (number, decimal) - Points percentage when leading after 1st period away; higher is better.
  - **`away_trail_after_1_period`** (string) - Record (W-L-OT) when trailing after 1st period, away games.
  - **`away_trail_after_1_period_tsi`** (number, decimal) - Points percentage when trailing after 1st period away; higher is better within this negative context.
  - **`away_tie_after_1_period`** (string) - Record (W-L-OT) when tied after 1st period, away games.
  - **`away_tie_after_1_period_tsi`** (number, decimal) - Points percentage when tied after 1st period away; higher is better.
  - **`away_lead_after_2_periods`** (string) - Record (W-L-OT) when leading after 2nd period, away games.
  - **`away_lead_after_2_periods_tsi`** (number, decimal) - Points percentage when leading after 2nd period away; higher is better.
  - **`away_trail_after_2_periods`** (string) - Record (W-L-OT) when trailing after 2nd period, away games.
  - **`away_trail_after_2_periods_tsi`** (number, decimal) - Points percentage when trailing after 2nd period away; higher is better within this negative context.
  - **`away_tie_after_2_periods`** (string) - Record (W-L-OT) when tied after 2nd period, away games.
  - **`away_tie_after_2_periods_tsi`** (number, decimal) - Points percentage when tied after 2nd period away; higher is better.

> [!NOTE]
> **Data starts with the 2014-15 season**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/records_team_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/records_team_now/
```
<a name="records_team_{year}/team_abbrev/{team_abbrev}"></a>
### 3.22 Get miscellaneous records teams by year and specific team
- **Endpoint:** `/records_team_{year}/team_abbrev/{team_abbrev}/`
- **Method:** GET
- **Description:** Returns team miscellaneous situational records for the given season and specific team. For each team, provides Overall/Home/Away splits across several situations (e.g., scoring first, opponent scoring first, outshooting/outshot, one-goal games, and when leading/trailing/tied after periods). Each record is returned as a W-L-OT string plus a computed Team Points Percentage index (_tsi), where points percentage is calculated as (2*W + 1*OT) / (2*(W+L+OT)), rounded to 4 decimals.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{team_abbrev}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`overall_scoring_first`** (string) - Record (W-L-OT) when the team scores first, all games.
  - **`overall_scoring_first_tsi`** (number, decimal) - Points percentage when scoring first; higher is better.
  - **`overall_opponent_scores_first`** (string) - Record (W-L-OT) when the opponent scores first, all games.
  - **`overall_opponent_scores_first_tsi`** (number, decimal) - Points percentage when conceding first; higher is better within this negative context (resilience).
  - **`overall_when_outshooting_opponent`** (string) - Record (W-L-OT) when outshooting the opponent, all games.
  - **`overall_when_outshooting_opponent_tsi`** (number, decimal) - Points percentage when outshooting the opponent; higher is better.
  - **`overall_when_outshot_opponent`** (string) - Record (W-L-OT) when being outshot by the opponent, all games.
  - **`overall_when_outshot_opponent_tsi`** (number, decimal) - Points percentage when outshot; higher is better within this negative context (withstanding pressure).
  - **`overall_1_goal_games`** (string) - Record (W-L-OT) in one-goal games, all games.
  - **`overall_1_goal_games_tsi`** (number, decimal) - Points percentage in one-goal games; higher is better.
  - **`overall_lead_after_1_period`** (string) - Record (W-L-OT) when leading after 1st period, all games.
  - **`overall_lead_after_1_period_tsi`** (number, decimal) - Points percentage when leading after 1st period; higher is better (closing out from early lead).
  - **`overall_trail_after_1_period`** (string) - Record (W-L-OT) when trailing after 1st period, all games.
  - **`overall_trail_after_1_period_tsi`** (number, decimal) - Points percentage when trailing after 1st period; higher is better within this negative context (comeback ability).
  - **`overall_tie_after_1_period`** (string) - Record (W-L-OT) when tied after 1st period, all games.
  - **`overall_tie_after_1_period_tsi`** (number, decimal) - Points percentage when tied after 1st period; higher is better.
  - **`overall_lead_after_2_periods`** (string) - Record (W-L-OT) when leading after 2nd period, all games.
  - **`overall_lead_after_2_periods_tsi`** (number, decimal) - Points percentage when leading after 2nd period; higher is better (finish ability).
  - **`overall_trail_after_2_periods`** (string) - Record (W-L-OT) when trailing after 2nd period, all games.
  - **`overall_trail_after_2_periods_tsi`** (number, decimal) - Points percentage when trailing after 2nd period; higher is better within this negative context (late resilience).
  - **`overall_tie_after_2_periods`** (string) - Record (W-L-OT) when tied after 2nd period, all games.
  - **`overall_tie_after_2_periods_tsi`** (number, decimal) - Points percentage when tied after 2nd period; higher is better.
  - **`home_scoring_first`** (string) - Record (W-L-OT) when the team scores first, home games.
  - **`home_scoring_first_tsi `** (number, decimal) - Points percentage when scoring first at home; higher is better.
  - **`home_opponent_scores_first`** (string) - Record (W-L-OT) when the opponent scores first, home games.
  - **`home_opponent_scores_first_tsi`** (number, decimal) - Points percentage when conceding first at home; higher is better within this negative context.
  - **`home_when_outshooting_opponent`** (string) - Record (W-L-OT) when outshooting the opponent, home games.
  - **`home_when_outshooting_opponent_tsi`** (number, decimal) - Points percentage when outshooting at home; higher is better.
  - **`home_when_outshot_opponent`** (string) - Record (W-L-OT) when being outshot by the opponent, home games.
  - **`home_when_outshot_opponent_tsi`** (number, decimal) - Points percentage when outshot at home; higher is better within this negative context.
  - **`home_1_goal_games`** (string) - Record (W-L-OT) in one-goal games, home games.
  - **`home_1_goal_games_tsi`** (number, decimal) - Points percentage in one-goal games at home; higher is better.
  - **`home_lead_after_1_period`** (string) - Record (W-L-OT) when leading after 1st period, home games.
  - **`home_lead_after_1_period_tsi`** (number, decimal) - Points percentage when leading after 1st period at home; higher is better.
  - **`home_trail_after_1_period`** (string) - Record (W-L-OT) when trailing after 1st period, home games.
  - **`home_trail_after_1_period_tsi`** (number, decimal) - Points percentage when trailing after 1st period at home; higher is better within this negative context.
  - **`home_tie_after_1_period`** (string) - Record (W-L-OT) when tied after 1st period, home games.
  - **`home_tie_after_1_period_tsi`** (number, decimal) - Points percentage when tied after 1st period at home; higher is better.
  - **`home_lead_after_2_periods`** (string) - Record (W-L-OT) when leading after 2nd period, home games.
  - **`home_lead_after_2_periods_tsi`** (number, decimal) - Points percentage when leading after 2nd period at home; higher is better.
  - **`home_trail_after_2_periods`** (string) - Record (W-L-OT) when trailing after 2nd period, home games.
  - **`home_trail_after_2_periods_tsi`** (number, decimal) - Points percentage when trailing after 2nd period at home; higher is better within this negative context.
  - **`home_tie_after_2_periods`** (string) - Record (W-L-OT) when tied after 2nd period, home games.
  - **`home_tie_after_2_periods_tsi`** (number, decimal) - Points percentage when tied after 2nd period at home; higher is better.
  - **`away_scoring_first`** (string) - Record (W-L-OT) when the team scores first, away games.
  - **`away_scoring_first_tsi`** (number, decimal) - Points percentage when scoring first away; higher is better.
  - **`away_opponent_scores_first`** (string) - Record (W-L-OT) when the opponent scores first, away games.
  - **`away_opponent_scores_first_tsi`** (number, decimal) - Points percentage when conceding first away; higher is better within this negative context.
  - **`away_when_outshooting_opponent`** (string) - Record (W-L-OT) when outshooting the opponent, away games.
  - **`away_when_outshooting_opponent_tsi`** (number, decimal) - Points percentage when outshooting away; higher is better.
  - **`away_when_outshot_opponent`** (string) - Record (W-L-OT) when being outshot by the opponent, away games.
  - **`away_when_outshot_opponent_tsi`** (number, decimal) - Points percentage when outshot away; higher is better within this negative context.
  - **`away_1_goal_games`** (string) - Record (W-L-OT) in one-goal games, away games.
  - **`away_1_goal_games_tsi`** (number, decimal) - Points percentage in one-goal games away; higher is better.
  - **`away_lead_after_1_period`** (string) - Record (W-L-OT) when leading after 1st period, away games.
  - **`away_lead_after_1_period_tsi`** (number, decimal) - Points percentage when leading after 1st period away; higher is better.
  - **`away_trail_after_1_period`** (string) - Record (W-L-OT) when trailing after 1st period, away games.
  - **`away_trail_after_1_period_tsi`** (number, decimal) - Points percentage when trailing after 1st period away; higher is better within this negative context.
  - **`away_tie_after_1_period`** (string) - Record (W-L-OT) when tied after 1st period, away games.
  - **`away_tie_after_1_period_tsi`** (number, decimal) - Points percentage when tied after 1st period away; higher is better.
  - **`away_lead_after_2_periods`** (string) - Record (W-L-OT) when leading after 2nd period, away games.
  - **`away_lead_after_2_periods_tsi`** (number, decimal) - Points percentage when leading after 2nd period away; higher is better.
  - **`away_trail_after_2_periods`** (string) - Record (W-L-OT) when trailing after 2nd period, away games.
  - **`away_trail_after_2_periods_tsi`** (number, decimal) - Points percentage when trailing after 2nd period away; higher is better within this negative context.
  - **`away_tie_after_2_periods`** (string) - Record (W-L-OT) when tied after 2nd period, away games.
  - **`away_tie_after_2_periods_tsi`** (number, decimal) - Points percentage when tied after 2nd period away; higher is better.

> [!NOTE]
> **Data starts with the 2014-15 season**

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/records_team_20212022/team_abbrev/WPG/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/records_team_now/team_abbrev/WPG/
```
---
<a name="season"></a>
## 4. Season  
<a name="season_summary_{year}"></a>
### 4.1 Get summary statistic season by year
- **Endpoint:** `/season_summary_{year}/`
- **Method:** GET
- **Description:** Get summary statistics for all teams for a specific season years
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`team_name`** (string) - Full team name. The name of the NHL team.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`conference`** (string) - Conference the team played in during the season. 
  - **`division`** (string) - Division the team played in during the season. 
  - **`playoff`** (string) - Indicator if the team made the playoffs that season (e.g., 'Yes', 'No).
  - **`games`** (integer) - Games Played. Total number of games played by the team during the regular season.
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout.
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout.
  - **`losses_ot`** (integer) - Overtime/Shootout Losses. Total number of games lost by the team in overtime or shootout (relevant from 2000 season onward).
  - **`points`** (integer) - Points. Total points accumulated by the team during the regular season.
  - **`points_pct`** (number, decimal) - Points percentage (i.e., points divided by maximum points). Expressed as a decimal (e.g., 0.494).
  - **`goals`** (integer) - Goals For (includes shootout wins).
  - **`goals_against`** (integer) - Goals Against (includes shootout losses).
  - **`srs`** (number, decimal) - Simple Rating System. A team rating that takes into account average goal differential and strength of schedule. The rating is denominated in goals above/below average, where zero is average. Expressed as a decimal (e.g., -1.29).
  - **`sos`** (number, decimal) - Strength of Schedule. A rating of strength of schedule. The rating is denominated in goals above/below average, where zero is average. Expressed as a decimal (e.g., -0.04).
  - **`reg_wins`** (integer) - Wins in Regulation.
  - **`points_pct_old`** (number, decimal) - Points percentage counting no points for OT loss, and any shootout game as a tie. i.e. pre-2000 situation. Expressed as a decimal (e.g., 0.488).
  - **`reg_rec`** (string) - Regulation time record (W-L-T/O format likely) in regulation time only. W(reg_wins)- L(losses)- T/O(wins - reg_wins + losses_ot).
  - **`points_pct_reg`** (number, decimal) - Points percentage based only on regulation time results. Expressed as a decimal (e.g., 0.598).

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/season_summary_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/season_summary_now/
```
<a name="season_summary_{year}/team_abbrev/{team_abbrev}"></a>
### 4.2 Get summary statistic season by year and specific team 
- **Endpoint:** `/season_summary_{year}/team_abbrev/{team_abbrev}`
- **Method:** GET
- **Description:** Get summary statistics for a specific team for a specific season year
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{abbreviation}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`team_name`** (string) - Full team name. The name of the NHL team.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`conference`** (string) - Conference the team played in during the season. 
  - **`division`** (string) - Division the team played in during the season. 
  - **`playoff`** (string) - Indicator if the team made the playoffs that season (e.g., 'Yes', 'No).
  - **`games`** (integer) - Games Played. Total number of games played by the team during the regular season.
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout.
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout.
  - **`losses_ot`** (integer) - Overtime/Shootout Losses. Total number of games lost by the team in overtime or shootout (relevant from 2000 season onward).
  - **`points`** (integer) - Points. Total points accumulated by the team during the regular season.
  - **`points_pct`** (number, decimal) - Points percentage (i.e., points divided by maximum points). Expressed as a decimal (e.g., 0.494).
  - **`goals`** (integer) - Goals For (includes shootout wins).
  - **`goals_against`** (integer) - Goals Against (includes shootout losses).
  - **`srs`** (number, decimal) - Simple Rating System. A team rating that takes into account average goal differential and strength of schedule. The rating is denominated in goals above/below average, where zero is average. Expressed as a decimal (e.g., -1.29).
  - **`sos`** (number, decimal) - Strength of Schedule. A rating of strength of schedule. The rating is denominated in goals above/below average, where zero is average. Expressed as a decimal (e.g., -0.04).
  - **`reg_wins`** (integer) - Wins in Regulation.
  - **`points_pct_old`** (number, decimal) - Points percentage counting no points for OT loss, and any shootout game as a tie. i.e. pre-2000 situation. Expressed as a decimal (e.g., 0.488).
  - **`reg_rec`** (string) - Regulation time record (W-L-T/O format likely) in regulation time only. W(reg_wins)- L(losses)- T/O(wins - reg_wins + losses_ot).
  - **`points_pct_reg`** (number, decimal) - Points percentage based only on regulation time results. Expressed as a decimal (e.g., 0.598).

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/season_summary_20212022/team_abbrev/TOR/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/season_summary_now/team_abbrev/TOR/
```
<a name="season_statistics_{year}"></a>
### 4.3 Get detail statistic season by year
- **Endpoint:** `/season_statistics_{year}/`
- **Method:** GET
- **Description:** Detail statistics of all teams for the specific season
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank. The ranking of the team in the league based on their performance. A lower number (e.g., 1) indicates a higher-ranked team.
  - **`team_name`** (string) - Full team name. The name of the NHL team.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`average_age`** (number, decimal) - Average Age. Average age of team weighted by time on ice. Expressed as a decimal (e.g., 25.7).
  - **`playoff`** (string) - Indicator if the team made the playoffs that season (e.g., 'Yes', 'No).
  - **`games`** (integer) - Games Played. Total number of games played by the team during the regular season.
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout.
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout.
  - **`losses_ot`** (integer) - Overtime/Shootout Losses. Total number of games lost by the team in overtime or shootout (relevant from 2000 season onward).
  - **`points`** (integer) - Points. Total points accumulated by the team during the regular season.
  - **`points_pct`** (number, decimal) - Points percentage (i.e., points divided by maximum points). Expressed as a decimal (e.g., 0.677).
  - **`goals`** (integer) - Goals For. Total number of goals scored by the team during the season. Reflects the team's offensive performance.
  - **`goals_against`** (integer) - Goals Against. Total number of goals conceded by the team during the season. Reflects the team's defensive performance.
  - **`wins_shootout`** (integer) - Shootout Wins. Total number of games won by the team in shootouts.
  - **`losses_shootout`** (integer) - Shootout Losses. Total number of games lost by the team in shootouts.
  - **`srs`** (number, decimal) - Simple Rating System. A team rating that takes into account average goal differential and strength of schedule. The rating is denominated in goals above/below average, where zero is average. Expressed as a decimal (e.g., -1.29).
  - **`sos`** (number, decimal) - Strength of Schedule. A rating of strength of schedule. The rating is denominated in goals above/below average, where zero is average. Expressed as a decimal (e.g., -0.05).
  - **`goals_for_per_game`** (number, decimal) - Goals For Per Game. Reflects offensive efficiency. Expressed as a decimal (e.g., 3.68).
  - **`goals_against_per_game`** (number, decimal) - Goals Against Per Game. Reflects defensive efficiency. Expressed as a decimal (e.g., 3.33).
  - **`goals_pp`** (integer) - Power Play Goals. Indicates power play effectiveness.
  - **`chances_pp`** (integer) - Power Play Opportunities. Reflects chances to use man advantage.
  - **`power_play_pct`** (number, decimal) - Power Play Percentage. Reflected the percentage of a team's power play opportunities that resulted in a goal. Expressed as a decimal (e.g., 22.45).
  - **`opp_goals_pp`** (integer) - Power Play Goals Against. Total number of goals conceded by the team during opposing power plays. Reflects penalty-killing effectiveness.
  - **`opp_chances_pp`** (integer) - Power Play Opportunities Against. Total number of power play opportunities the opposing team had against them. Indicates how often the team had to kill penalties.
  - **`pen_kill_pct`** (number, decimal) - Penalty Kill Percentage. Percentage of opposing power play opportunities successfully killed off. Higher percentages indicate better penalty-killing performance. Expressed as a decimal (e.g., 82.47).
  - **`goals_sh`** (integer) - Short-Handed Goals. Reflected the number of goals a team scored while playing short-handed (with fewer players on the ice, usually due to a penalty).
  - **`opp_goals_sh`** (integer) - Short-Handed Goals Against. Reflected the number of goals a team allowed while they were on a power play, meaning the opposing (penalized) team scored despite being short-handed.
  - **`pen_min_per_game`** (number, decimal) - Penalties in Minutes Per Game. Reflects the team's discipline or lack thereof. Expressed as a decimal (e.g., 13.6).
  - **`pen_min_per_game_opp`** (number, decimal) - Opponent Penalties in Minutes Per Game. Average number of penalty minutes per game for the opposing team. Expressed as a decimal (e.g., 9.9).
  - **`shots`** (integer) - Shots on Goal. Total number of shots on goal taken by the team during the season. Reflects offensive activity.
  - **`shot_pct`** (number, decimal) - Shooting Percentage. Percentage of shots on goal that resulted in goals. Expressed as a decimal (e.g., 11.6).
  - **`shots_against`** (integer) - Shots Against. Total number of shots on goal taken by opponents against the team. Reflects defensive pressure faced.
  - **`save_pct`** (number, decimal) - Save Percentage. Percentage of shots on goal stopped by the team's goaltenders. Higher values mean better goaltending. Expressed as a decimal (e.g., 0.901).
  - **`shutouts`** (integer) - Shutouts. Total number of games in which the team did not allow any goals. Reflects strong defensive and goaltending performances.

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/season_statistics_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/season_statistics_now/
```
<a name="season_statistics_{year}/team_abbrev/{team_abbrev}"></a>
### 4.4 Get detail statistic season by year and specific team
- **Endpoint:** `/season_statistics_{year}/team_abbrev/{team_abbrev}/`
- **Method:** GET
- **Description:** Detail statistics of a specific team for specific season
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{team_abbrev}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank. The ranking of the team in the league based on their performance. A lower number (e.g., 1) indicates a higher-ranked team.
  - **`team_name`** (string) - Full team name. The name of the NHL team.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`average_age`** (number, decimal) - Average Age. Average age of team weighted by time on ice. Expressed as a decimal (e.g., 25.7).
  - **`playoff`** (string) - Indicator if the team made the playoffs that season (e.g., 'Yes', 'No).
  - **`games`** (integer) - Games Played. Total number of games played by the team during the regular season.
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout.
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout.
  - **`losses_ot`** (integer) - Overtime/Shootout Losses. Total number of games lost by the team in overtime or shootout (relevant from 2000 season onward).
  - **`points`** (integer) - Points. Total points accumulated by the team during the regular season.
  - **`points_pct`** (number, decimal) - Points percentage (i.e., points divided by maximum points). Expressed as a decimal (e.g., 0.677).
  - **`goals`** (integer) - Goals For. Total number of goals scored by the team during the season. Reflects the team's offensive performance.
  - **`goals_against`** (integer) - Goals Against. Total number of goals conceded by the team during the season. Reflects the team's defensive performance.
  - **`wins_shootout`** (integer) - Shootout Wins. Total number of games won by the team in shootouts.
  - **`losses_shootout`** (integer) - Shootout Losses. Total number of games lost by the team in shootouts.
  - **`srs`** (number, decimal) - Simple Rating System. A team rating that takes into account average goal differential and strength of schedule. The rating is denominated in goals above/below average, where zero is average. Expressed as a decimal (e.g., -1.29).
  - **`sos`** (number, decimal) - Strength of Schedule. A rating of strength of schedule. The rating is denominated in goals above/below average, where zero is average. Expressed as a decimal (e.g., -0.05).
  - **`goals_for_per_game`** (number, decimal) - Goals For Per Game. Reflects offensive efficiency. Expressed as a decimal (e.g., 3.68).
  - **`goals_against_per_game`** (number, decimal) - Goals Against Per Game. Reflects defensive efficiency. Expressed as a decimal (e.g., 3.33).
  - **`goals_pp`** (integer) - Power Play Goals. Indicates power play effectiveness.
  - **`chances_pp`** (integer) - Power Play Opportunities. Reflects chances to use man advantage.
  - **`power_play_pct`** (number, decimal) - Power Play Percentage. Reflected the percentage of a team's power play opportunities that resulted in a goal. Expressed as a decimal (e.g., 22.45).
  - **`opp_goals_pp`** (integer) - Power Play Goals Against. Total number of goals conceded by the team during opposing power plays. Reflects penalty-killing effectiveness.
  - **`opp_chances_pp`** (integer) - Power Play Opportunities Against. Total number of power play opportunities the opposing team had against them. Indicates how often the team had to kill penalties.
  - **`pen_kill_pct`** (number, decimal) - Penalty Kill Percentage. Percentage of opposing power play opportunities successfully killed off. Higher percentages indicate better penalty-killing performance. Expressed as a decimal (e.g., 82.47).
  - **`goals_sh`** (integer) - Short-Handed Goals. Reflected the number of goals a team scored while playing short-handed (with fewer players on the ice, usually due to a penalty).
  - **`opp_goals_sh`** (integer) - Short-Handed Goals Against. Reflected the number of goals a team allowed while they were on a power play, meaning the opposing (penalized) team scored despite being short-handed.
  - **`pen_min_per_game`** (number, decimal) - Penalties in Minutes Per Game. Reflects the team's discipline or lack thereof. Expressed as a decimal (e.g., 13.6).
  - **`pen_min_per_game_opp`** (number, decimal) - Opponent Penalties in Minutes Per Game. Average number of penalty minutes per game for the opposing team. Expressed as a decimal (e.g., 9.9).
  - **`shots`** (integer) - Shots on Goal. Total number of shots on goal taken by the team during the season. Reflects offensive activity.
  - **`shot_pct`** (number, decimal) - Shooting Percentage. Percentage of shots on goal that resulted in goals. Expressed as a decimal (e.g., 11.6).
  - **`shots_against`** (integer) - Shots Against. Total number of shots on goal taken by opponents against the team. Reflects defensive pressure faced.
  - **`save_pct`** (number, decimal) - Save Percentage. Percentage of shots on goal stopped by the team's goaltenders. Higher values mean better goaltending. Expressed as a decimal (e.g., 0.901).
  - **`shutouts`** (integer) - Shutouts. Total number of games in which the team did not allow any goals. Reflects strong defensive and goaltending performances.

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/season_statistics_20212022/team_abbrev/TOR/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/season_statistics_now/team_abbrev/TOR/
```
<a name="season_statistics_{year}/rank/{rank}"></a>
### 4.5 Get detail statistic season by year and specific rank
- **Endpoint:** `/season_statistics_{year}/rank/{rank}`
- **Method:** GET
- **Description:** Detail statistics of a specific team for specific season and specific rank
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{rank}`** (string) - Rank. The ranking of the team in the league based on their performance. A lower number (e.g., 1) indicates a higher-ranked team.
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank. The ranking of the team in the league based on their performance. A lower number (e.g., 1) indicates a higher-ranked team.
  - **`team_name`** (string) - Full team name. The name of the NHL team.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`average_age`** (number, decimal) - Average Age. Average age of team weighted by time on ice. Expressed as a decimal (e.g., 25.7).
  - **`playoff`** (string) - Indicator if the team made the playoffs that season (e.g., 'Yes', 'No).
  - **`games`** (integer) - Games Played. Total number of games played by the team during the regular season.
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout.
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout.
  - **`losses_ot`** (integer) - Overtime/Shootout Losses. Total number of games lost by the team in overtime or shootout (relevant from 2000 season onward).
  - **`points`** (integer) - Points. Total points accumulated by the team during the regular season.
  - **`points_pct`** (number, decimal) - Points percentage (i.e., points divided by maximum points). Expressed as a decimal (e.g., 0.677).
  - **`goals`** (integer) - Goals For. Total number of goals scored by the team during the season. Reflects the team's offensive performance.
  - **`goals_against`** (integer) - Goals Against. Total number of goals conceded by the team during the season. Reflects the team's defensive performance.
  - **`wins_shootout`** (integer) - Shootout Wins. Total number of games won by the team in shootouts.
  - **`losses_shootout`** (integer) - Shootout Losses. Total number of games lost by the team in shootouts.
  - **`srs`** (number, decimal) - Simple Rating System. A team rating that takes into account average goal differential and strength of schedule. The rating is denominated in goals above/below average, where zero is average. Expressed as a decimal (e.g., -1.29).
  - **`sos`** (number, decimal) - Strength of Schedule. A rating of strength of schedule. The rating is denominated in goals above/below average, where zero is average. Expressed as a decimal (e.g., -0.05).
  - **`goals_for_per_game`** (number, decimal) - Goals For Per Game. Reflects offensive efficiency. Expressed as a decimal (e.g., 3.68).
  - **`goals_against_per_game`** (number, decimal) - Goals Against Per Game. Reflects defensive efficiency. Expressed as a decimal (e.g., 3.33).
  - **`goals_pp`** (integer) - Power Play Goals. Indicates power play effectiveness.
  - **`chances_pp`** (integer) - Power Play Opportunities. Reflects chances to use man advantage.
  - **`power_play_pct`** (number, decimal) - Power Play Percentage. Reflected the percentage of a team's power play opportunities that resulted in a goal. Expressed as a decimal (e.g., 22.45).
  - **`opp_goals_pp`** (integer) - Power Play Goals Against. Total number of goals conceded by the team during opposing power plays. Reflects penalty-killing effectiveness.
  - **`opp_chances_pp`** (integer) - Power Play Opportunities Against. Total number of power play opportunities the opposing team had against them. Indicates how often the team had to kill penalties.
  - **`pen_kill_pct`** (number, decimal) - Penalty Kill Percentage. Percentage of opposing power play opportunities successfully killed off. Higher percentages indicate better penalty-killing performance. Expressed as a decimal (e.g., 82.47).
  - **`goals_sh`** (integer) - Short-Handed Goals. Reflected the number of goals a team scored while playing short-handed (with fewer players on the ice, usually due to a penalty).
  - **`opp_goals_sh`** (integer) - Short-Handed Goals Against. Reflected the number of goals a team allowed while they were on a power play, meaning the opposing (penalized) team scored despite being short-handed.
  - **`pen_min_per_game`** (number, decimal) - Penalties in Minutes Per Game. Reflects the team's discipline or lack thereof. Expressed as a decimal (e.g., 13.6).
  - **`pen_min_per_game_opp`** (number, decimal) - Opponent Penalties in Minutes Per Game. Average number of penalty minutes per game for the opposing team. Expressed as a decimal (e.g., 9.9).
  - **`shots`** (integer) - Shots on Goal. Total number of shots on goal taken by the team during the season. Reflects offensive activity.
  - **`shot_pct`** (number, decimal) - Shooting Percentage. Percentage of shots on goal that resulted in goals. Expressed as a decimal (e.g., 11.6).
  - **`shots_against`** (integer) - Shots Against. Total number of shots on goal taken by opponents against the team. Reflects defensive pressure faced.
  - **`save_pct`** (number, decimal) - Save Percentage. Percentage of shots on goal stopped by the team's goaltenders. Higher values mean better goaltending. Expressed as a decimal (e.g., 0.901).
  - **`shutouts`** (integer) - Shutouts. Total number of games in which the team did not allow any goals. Reflects strong defensive and goaltending performances.

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/season_statistics_20212022/rank/2/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/season_statistics_now/rank/2/
```
<a name="season_statistics_{year}/playoff/{playoff}"></a>
### 4.6 Get detail statistic season by year and playoff
- **Endpoint:** `/season_statistics_{year}/playoff/{playoff}`
- **Method:** GET
- **Description:** Detail statistics of a specific team for specific season and playoff
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{playoff}`** (string) - Indicator if the team made the playoffs that season (e.g., 'Yes', 'No).
- **Response:** JSON format
- **Schema table:**
  - **`rank`** (integer) - Rank. The ranking of the team in the league based on their performance. A lower number (e.g., 1) indicates a higher-ranked team.
  - **`team_name`** (string) - Full team name. The name of the NHL team.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`average_age`** (number, decimal) - Average Age. Average age of team weighted by time on ice. Expressed as a decimal (e.g., 25.7).
  - **`playoff`** (string) - Indicator if the team made the playoffs that season (e.g., 'Yes', 'No).
  - **`games`** (integer) - Games Played. Total number of games played by the team during the regular season.
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout.
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout.
  - **`losses_ot`** (integer) - Overtime/Shootout Losses. Total number of games lost by the team in overtime or shootout (relevant from 2000 season onward).
  - **`points`** (integer) - Points. Total points accumulated by the team during the regular season.
  - **`points_pct`** (number, decimal) - Points percentage (i.e., points divided by maximum points). Expressed as a decimal (e.g., 0.677).
  - **`goals`** (integer) - Goals For. Total number of goals scored by the team during the season. Reflects the team's offensive performance.
  - **`goals_against`** (integer) - Goals Against. Total number of goals conceded by the team during the season. Reflects the team's defensive performance.
  - **`wins_shootout`** (integer) - Shootout Wins. Total number of games won by the team in shootouts.
  - **`losses_shootout`** (integer) - Shootout Losses. Total number of games lost by the team in shootouts.
  - **`srs`** (number, decimal) - Simple Rating System. A team rating that takes into account average goal differential and strength of schedule. The rating is denominated in goals above/below average, where zero is average. Expressed as a decimal (e.g., -1.29).
  - **`sos`** (number, decimal) - Strength of Schedule. A rating of strength of schedule. The rating is denominated in goals above/below average, where zero is average. Expressed as a decimal (e.g., -0.05).
  - **`goals_for_per_game`** (number, decimal) - Goals For Per Game. Reflects offensive efficiency. Expressed as a decimal (e.g., 3.68).
  - **`goals_against_per_game`** (number, decimal) - Goals Against Per Game. Reflects defensive efficiency. Expressed as a decimal (e.g., 3.33).
  - **`goals_pp`** (integer) - Power Play Goals. Indicates power play effectiveness.
  - **`chances_pp`** (integer) - Power Play Opportunities. Reflects chances to use man advantage.
  - **`power_play_pct`** (number, decimal) - Power Play Percentage. Reflected the percentage of a team's power play opportunities that resulted in a goal. Expressed as a decimal (e.g., 22.45).
  - **`opp_goals_pp`** (integer) - Power Play Goals Against. Total number of goals conceded by the team during opposing power plays. Reflects penalty-killing effectiveness.
  - **`opp_chances_pp`** (integer) - Power Play Opportunities Against. Total number of power play opportunities the opposing team had against them. Indicates how often the team had to kill penalties.
  - **`pen_kill_pct`** (number, decimal) - Penalty Kill Percentage. Percentage of opposing power play opportunities successfully killed off. Higher percentages indicate better penalty-killing performance. Expressed as a decimal (e.g., 82.47).
  - **`goals_sh`** (integer) - Short-Handed Goals. Reflected the number of goals a team scored while playing short-handed (with fewer players on the ice, usually due to a penalty).
  - **`opp_goals_sh`** (integer) - Short-Handed Goals Against. Reflected the number of goals a team allowed while they were on a power play, meaning the opposing (penalized) team scored despite being short-handed.
  - **`pen_min_per_game`** (number, decimal) - Penalties in Minutes Per Game. Reflects the team's discipline or lack thereof. Expressed as a decimal (e.g., 13.6).
  - **`pen_min_per_game_opp`** (number, decimal) - Opponent Penalties in Minutes Per Game. Average number of penalty minutes per game for the opposing team. Expressed as a decimal (e.g., 9.9).
  - **`shots`** (integer) - Shots on Goal. Total number of shots on goal taken by the team during the season. Reflects offensive activity.
  - **`shot_pct`** (number, decimal) - Shooting Percentage. Percentage of shots on goal that resulted in goals. Expressed as a decimal (e.g., 11.6).
  - **`shots_against`** (integer) - Shots Against. Total number of shots on goal taken by opponents against the team. Reflects defensive pressure faced.
  - **`save_pct`** (number, decimal) - Save Percentage. Percentage of shots on goal stopped by the team's goaltenders. Higher values mean better goaltending. Expressed as a decimal (e.g., 0.901).
  - **`shutouts`** (integer) - Shutouts. Total number of games in which the team did not allow any goals. Reflects strong defensive and goaltending performances.

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/season_statistics_20212022/playoff/yes/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/season_statistics_now/playoff/yes/
```
<a name="league_average_{year}"></a>
### 4.7 Get league average by year
- **Endpoint:** `/league_average_{year}/`
- **Method:** GET
- **Description:** League average for the specific season
- **Parameters:**
   - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`average_age`** (number, decimal) - Average Age. Average age of team weighted by time on ice. Expressed as a decimal (e.g., 27.4).
  - **`games`** (integer) - Games Played. Total number of games played by the team during the regular season.
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout. (average value)
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout. (average value)
  - **`losses_ot`** (integer) - Overtime/Shootout Losses. Total number of games lost by the team in overtime or shootout (relevant from 2000 season onward). (average value)
  - **`points`** (integer) - Points. Total number of points earned by a team in the standings. Usually, teams receive two points for a win, one point for an overtime or shootout loss, and zero points for a regulation loss. Reflects a team's overall success and position relative to other teams in the league. (average value)
  - **`points_pct`** (number, decimal) - Points percentage (i.e., points divided by maximum points). Expressed as a decimal (e.g., 0.558). (average value)
  - **`goals`** (integer) - Goals For. Total goals scored by the team. Shows offensive output. (average value)
  - **`goals_against`** (integer) - Goals Against. Total goals allowed by the team. Shows defensive strength. (average value)
  - **`goals_pp`** (integer) - Power Play Goals. Total goals scored by the team while on a power play. Indicates power play effectiveness. (average value)
  - **`chances_pp`** (integer) - Power Play Opportunities. Total number of times the team had a power play. Reflects chances to use man advantage. (average value)
  - **`power_play_pct`** (number, decimal) - Power Play Percentage. Percentage of power plays on which the team scored. Higher values indicate better power play performance. Expressed as a decimal (e.g., 20.03). (average value)
  - **`opp_goals_pp`** (integer) - Power Play Goals Against. Total number of goals conceded by the team during opposing power plays. Reflects penalty-killing effectiveness. (average value)
  - **`opp_chances_pp`** (integer) - Power Play Opportunities Against. Total number of power play opportunities the opposing team had against them. Indicates how often the team had to kill penalties. (average value)
  - **`pen_kill_pct`** (number, decimal) - Penalty Kill Percentage. Percentage of opposing power play opportunities successfully killed off. Higher percentages indicate better penalty-killing performance. Expressed as a decimal (e.g., 0.837). (average value)
  - **`goals_sh`** (integer) - Short-Handed Goals (SH). Total number of short-handed goals scored by the team. Goals scored while the team was on the penalty kill. (average value)
  - **`opp_goals_sh`** (integer) - Short-Handed Goals Against (SHA). Total number of short-handed goals conceded by the team. Goals scored by the opposing team while on the penalty kill. (average value)
  - **`pen_min_per_game`** (number, decimal) - Penalties in Minutes Per Game. Average number of penalty minutes per game for the team. Reflects the team's discipline or lack thereof. Expressed as a decimal (e.g., 8.3). (average value)
  - **`pen_min_per_game_opp`** (number, decimal) - Opponent Penalties in Minutes Per Game. Average number of penalty minutes per game for the opposing team. Shows how often rivals are penalized (e.g., 8.3) (average value)
  - **`shots`** (integer) - Shots on Goal. Total number of shots on goal taken by the team during the season. Reflects offensive activity. (average value)
  - **`shot_pct`** (number, decimal) - Shooting Percentage. Percentage of shots on goal that resulted in goals. Expressed as a decimal (e.g., 9.5). (average value)
  - **`shots_against`** (integer) - Shots Against. Total number of shots on goal taken by opponents against the team. Reflects defensive pressure faced. (average value)
  - **`save_pct`** (number, decimal) - Save Percentage. Percentage of shots on goal stopped by the team's goaltenders. Higher values mean better goaltending. Expressed as a decimal (e.g., 0.905). (average value)
  - **`shutouts`** (integer) - Shutouts. Total number of games in which the team did not allow any goals. Reflects strong defensive and goaltending performances. (average value)

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_average_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_average_now/
```
<a name="regular_season_schedule_{year}"></a>
### 4.8 Get regular season schedule by year
- **Endpoint:** `/regular_season_schedule_{year}/`
- **Method:** GET
- **Description:** Table with schedule and results for all regular season games for the specified year. 
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`game_id`** (string) – Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`game_date`** (date) –  Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_time`** (string) – Game Time. Scheduled local start time of the game in 12-hour format; or null if unknown (e.g., "10:00 PM").
  - **`away_team_name`** (string) – Away Team Name. Full name of the visiting team (e.g., "Toronto Maple Leafs").
  - **`away_team_abbrev`** (string) –  Away Team Abbreviation. Official abbreviation (e.g., "TOR").
  - **`away_team_goals`** (integer) – Away Team Goals. Goals scored by away team; null if not played (e.g., 2).
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team (e.g., "Montreal Canadiens").
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Official abbreviation (e.g., "MTL").
  - **`home_team_goals`** (integer) –  Home Team Goals. Goals scored by home team; null if not played (e.g., 3).
  - **`overtime`** (string) –  Overtime or Shootout. "OT", "2OT", "SO" or null if decided in regulation.
  - **`attendance `** (integer) – Attendance. Number of spectators at the game; null if not available (e.g., 21047).
  - **`game_duration`** (string) – Game Duration. Length of game in hours and minutes "H:MM"; null if not played (e.g., "2:33").

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/regular_season_schedule_{year}/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/regular_season_schedule_now/
```
<a name="regular_season_schedule_{year}/game_date/{game_date}"></a>
### 4.9 Get regular season schedule by year and specific date
- **Endpoint:** `/regular_season_schedule_{year}/game_date/{game_date}`
- **Method:** GET
- **Description:** Table with schedule and results for all games played on a specific date within the chosen season.
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
     - **`game_date`** (date) - Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
- **Response:** JSON format
- **Schema table:**
  - **`game_id`** (string) – Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`game_date`** (date) –  Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_time`** (string) – Game Time. Scheduled local start time of the game in 12-hour format; or null if unknown (e.g., "10:00 PM").
  - **`away_team_name`** (string) – Away Team Name. Full name of the visiting team (e.g., "Toronto Maple Leafs").
  - **`away_team_abbrev`** (string) –  Away Team Abbreviation. Official abbreviation (e.g., "TOR").
  - **`away_team_goals`** (integer) – Away Team Goals. Goals scored by away team; null if not played (e.g., 2).
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team (e.g., "Montreal Canadiens").
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Official abbreviation (e.g., "MTL").
  - **`home_team_goals`** (integer) –  Home Team Goals. Goals scored by home team; null if not played (e.g., 3).
  - **`overtime`** (string) –  Overtime or Shootout. "OT", "2OT", "SO" or null if decided in regulation.
  - **`attendance `** (integer) – Attendance. Number of spectators at the game; null if not available (e.g., 21047).
  - **`game_duration`** (string) – Game Duration. Length of game in hours and minutes "H:MM"; null if not played (e.g., "2:33").

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/regular_season_schedule_{year}/game_date/{game_date}/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/regular_season_schedule_now/game_date/{game_date}/
```
<a name="regular_season_schedule_{year}/game_id/{game_id}"></a>
### 4.10 Get regular season schedule by year and specific date
- **Endpoint:** `/regular_season_schedule_{year}/game_id/{game_id}`
- **Method:** GET
- **Description:** Information about a specific game by its unique game ID.
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
     - **`game_id`** (string) - Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
- **Response:** JSON format
- **Schema table:**
  - **`game_id`** (string) – Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`game_date`** (date) –  Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_time`** (string) – Game Time. Scheduled local start time of the game in 12-hour format; or null if unknown (e.g., "10:00 PM").
  - **`away_team_name`** (string) – Away Team Name. Full name of the visiting team (e.g., "Toronto Maple Leafs").
  - **`away_team_abbrev`** (string) –  Away Team Abbreviation. Official abbreviation (e.g., "TOR").
  - **`away_team_goals`** (integer) – Away Team Goals. Goals scored by away team; null if not played (e.g., 2).
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team (e.g., "Montreal Canadiens").
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Official abbreviation (e.g., "MTL").
  - **`home_team_goals`** (integer) –  Home Team Goals. Goals scored by home team; null if not played (e.g., 3).
  - **`overtime`** (string) –  Overtime or Shootout. "OT", "2OT", "SO" or null if decided in regulation.
  - **`attendance `** (integer) – Attendance. Number of spectators at the game; null if not available (e.g., 21047).
  - **`game_duration`** (string) – Game Duration. Length of game in hours and minutes "H:MM"; null if not played (e.g., "2:33").

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/regular_season_schedule_{year}/game_id/{game_id}/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/regular_season_schedule_now/game_id/{game_id}/
```
<a name="regular_season_schedule_{year}/team_abbrev/{team_abbrev}"></a>
### 4.11 Get regular season schedule by year and specific team
- **Endpoint:** `/regular_season_schedule_{year}/team_abbrev/{team_abbrev}`
- **Method:** GET
- **Description:** Table with all games for a specific team in the selected season.
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
     - **`team_abbrev`** (string) - Team's official abbreviation (e.g., "TOR").
- **Response:** JSON format
- **Schema table:**
  - **`game_id`** (string) – Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`game_date`** (date) –  Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_time`** (string) – Game Time. Scheduled local start time of the game in 12-hour format; or null if unknown (e.g., "10:00 PM").
  - **`away_team_name`** (string) – Away Team Name. Full name of the visiting team (e.g., "Toronto Maple Leafs").
  - **`away_team_abbrev`** (string) –  Away Team Abbreviation. Official abbreviation (e.g., "TOR").
  - **`away_team_goals`** (integer) – Away Team Goals. Goals scored by away team; null if not played (e.g., 2).
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team (e.g., "Montreal Canadiens").
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Official abbreviation (e.g., "MTL").
  - **`home_team_goals`** (integer) –  Home Team Goals. Goals scored by home team; null if not played (e.g., 3).
  - **`overtime`** (string) –  Overtime or Shootout. "OT", "2OT", "SO" or null if decided in regulation.
  - **`attendance `** (integer) – Attendance. Number of spectators at the game; null if not available (e.g., 21047).
  - **`game_duration`** (string) – Game Duration. Length of game in hours and minutes "H:MM"; null if not played (e.g., "2:33").

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/regular_season_schedule_{year}/team_abbrev/{team_abbrev}/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/regular_season_schedule_now/team_abbrev/{team_abbrev}/
```
<a name="regular_season_schedule_{year}/finished"></a>
### 4.12 Get regular season schedule by year and finished game
- **Endpoint:** `/regular_season_schedule_{year}/finished`
- **Method:** GET
- **Description:** Table with all finished (concluded) regular season games in the selected season.
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`game_id`** (string) – Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`game_date`** (date) –  Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_time`** (string) – Game Time. Scheduled local start time of the game in 12-hour format; or null if unknown (e.g., "10:00 PM").
  - **`away_team_name`** (string) – Away Team Name. Full name of the visiting team (e.g., "Toronto Maple Leafs").
  - **`away_team_abbrev`** (string) –  Away Team Abbreviation. Official abbreviation (e.g., "TOR").
  - **`away_team_goals`** (integer) – Away Team Goals. Goals scored by away team; null if not played (e.g., 2).
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team (e.g., "Montreal Canadiens").
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Official abbreviation (e.g., "MTL").
  - **`home_team_goals`** (integer) –  Home Team Goals. Goals scored by home team; null if not played (e.g., 3).
  - **`overtime`** (string) –  Overtime or Shootout. "OT", "2OT", "SO" or null if decided in regulation.
  - **`attendance `** (integer) – Attendance. Number of spectators at the game; null if not available (e.g., 21047).
  - **`game_duration`** (string) – Game Duration. Length of game in hours and minutes "H:MM"; null if not played (e.g., "2:33").

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/regular_season_schedule_{year}/finished/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/regular_season_schedule_now/finished/
```
<a name="regular_season_schedule_{year}/upcoming"></a>
### 4.13 Get regular season schedule by year and upcoming game
- **Endpoint:** `/regular_season_schedule_{year}/upcoming`
- **Method:** GET
- **Description:** Table with all upcoming games in the selected season.
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`game_id`** (string) – Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`game_date`** (date) –  Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_time`** (string) – Game Time. Scheduled local start time of the game in 12-hour format; or null if unknown (e.g., "10:00 PM").
  - **`away_team_name`** (string) – Away Team Name. Full name of the visiting team (e.g., "Toronto Maple Leafs").
  - **`away_team_abbrev`** (string) –  Away Team Abbreviation. Official abbreviation (e.g., "TOR").
  - **`away_team_goals`** (integer) – Away Team Goals. Goals scored by away team; null if not played (e.g., 2).
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team (e.g., "Montreal Canadiens").
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Official abbreviation (e.g., "MTL").
  - **`home_team_goals`** (integer) –  Home Team Goals. Goals scored by home team; null if not played (e.g., 3).
  - **`overtime`** (string) –  Overtime or Shootout. "OT", "2OT", "SO" or null if decided in regulation.
  - **`attendance `** (integer) – Attendance. Number of spectators at the game; null if not available (e.g., 21047).
  - **`game_duration`** (string) – Game Duration. Length of game in hours and minutes "H:MM"; null if not played (e.g., "2:33").

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/regular_season_schedule_{year}/upcoming/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/regular_season_schedule_now/upcoming/
```
<a name="regular_season_schedule_{year}/upcoming_day"></a>
### 4.14 Get regular season schedule by year and upcoming game for next day
- **Endpoint:** `/regular_season_schedule_{year}/upcoming_day`
- **Method:** GET
- **Description:** Table with all games scheduled for the next day in the selected season. If today is 06/25/2025 and the next first games will start only on 10/25/2025, it will take the date for 10/25/2025, since these are the first available games.
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`game_id`** (string) – Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`game_date`** (date) –  Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_time`** (string) – Game Time. Scheduled local start time of the game in 12-hour format; or null if unknown (e.g., "10:00 PM").
  - **`away_team_name`** (string) – Away Team Name. Full name of the visiting team (e.g., "Toronto Maple Leafs").
  - **`away_team_abbrev`** (string) –  Away Team Abbreviation. Official abbreviation (e.g., "TOR").
  - **`away_team_goals`** (integer) – Away Team Goals. Goals scored by away team; null if not played (e.g., 2).
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team (e.g., "Montreal Canadiens").
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Official abbreviation (e.g., "MTL").
  - **`home_team_goals`** (integer) –  Home Team Goals. Goals scored by home team; null if not played (e.g., 3).
  - **`overtime`** (string) –  Overtime or Shootout. "OT", "2OT", "SO" or null if decided in regulation.
  - **`attendance `** (integer) – Attendance. Number of spectators at the game; null if not available (e.g., 21047).
  - **`game_duration`** (string) – Game Duration. Length of game in hours and minutes "H:MM"; null if not played (e.g., "2:33").

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/regular_season_schedule_{year}/upcoming_day/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/regular_season_schedule_now/upcoming_day/
```
<a name="regular_season_schedule_{year}/upcoming_week"></a>
### 4.15 Get regular season schedule by year and upcoming game for next week
- **Endpoint:** `/regular_season_schedule_{year}/upcoming_week`
- **Method:** GET
- **Description:** Table with all games scheduled for the next week in the selected season.
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`game_id`** (string) – Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`game_date`** (date) –  Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_time`** (string) – Game Time. Scheduled local start time of the game in 12-hour format; or null if unknown (e.g., "10:00 PM").
  - **`away_team_name`** (string) – Away Team Name. Full name of the visiting team (e.g., "Toronto Maple Leafs").
  - **`away_team_abbrev`** (string) –  Away Team Abbreviation. Official abbreviation (e.g., "TOR").
  - **`away_team_goals`** (integer) – Away Team Goals. Goals scored by away team; null if not played (e.g., 2).
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team (e.g., "Montreal Canadiens").
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Official abbreviation (e.g., "MTL").
  - **`home_team_goals`** (integer) –  Home Team Goals. Goals scored by home team; null if not played (e.g., 3).
  - **`overtime`** (string) –  Overtime or Shootout. "OT", "2OT", "SO" or null if decided in regulation.
  - **`attendance `** (integer) – Attendance. Number of spectators at the game; null if not available (e.g., 21047).
  - **`game_duration`** (string) – Game Duration. Length of game in hours and minutes "H:MM"; null if not played (e.g., "2:33").

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/regular_season_schedule_{year}/upcoming_week/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/regular_season_schedule_now/upcoming_week/
```
<a name="regular_season_schedule_{year}/upcoming_month"></a>
### 4.16 Get regular season schedule by year and upcoming game for next month
- **Endpoint:** `/regular_season_schedule_{year}/upcoming_month`
- **Method:** GET
- **Description:** Table with all games scheduled for the next month in the selected season.
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`game_id`** (string) – Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`game_date`** (date) –  Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_time`** (string) – Game Time. Scheduled local start time of the game in 12-hour format; or null if unknown (e.g., "10:00 PM").
  - **`away_team_name`** (string) – Away Team Name. Full name of the visiting team (e.g., "Toronto Maple Leafs").
  - **`away_team_abbrev`** (string) –  Away Team Abbreviation. Official abbreviation (e.g., "TOR").
  - **`away_team_goals`** (integer) – Away Team Goals. Goals scored by away team; null if not played (e.g., 2).
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team (e.g., "Montreal Canadiens").
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Official abbreviation (e.g., "MTL").
  - **`home_team_goals`** (integer) –  Home Team Goals. Goals scored by home team; null if not played (e.g., 3).
  - **`overtime`** (string) –  Overtime or Shootout. "OT", "2OT", "SO" or null if decided in regulation.
  - **`attendance `** (integer) – Attendance. Number of spectators at the game; null if not available (e.g., 21047).
  - **`game_duration`** (string) – Game Duration. Length of game in hours and minutes "H:MM"; null if not played (e.g., "2:33").

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/regular_season_schedule_{year}/upcoming_month/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/regular_season_schedule_now/upcoming_month/
```
---
<a name="playoff"></a>
## 5. Playoff
<a name="league_playoff_series_result_{year}"></a>
### 5.1 Get playoff result by year
- **Endpoint:** `/league_playoff_series_result_{year}/`
- **Method:** GET
- **Description:** Table with results of games in playoff series. 
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) – Season ID. Unique identifier for the NHL season (e.g., 20212022).
  - **`game_id`** (string) – Game ID. Unique identifier for each playoff game.
  - **`round_name`** (string) – Round Name. The name or description of the playoff round (e.g., "Quarterfinals", "Stanley Cup Final").
  - **`game_number`** (string) – Game Number. The sequential number of the game within the series (e.g., "Game 5").
  - **`game_data`** (date) – Game Date. The date on which the playoff game was played (e.g., "2021-08-21").
  - **`away_team_name`** (string) – Away Team Name. Full name of the away (visiting) team.
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team.
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Three-letter abbreviation for the home team (e.g., "BOS").
  - **`away_team_score`** (integer) – Away Team Score. Number of goals scored by the away team in this game.
  - **`home_team_score`** (integer) – Home Team Score. Number of goals scored by the home team in this game.
  - **`winner_team_name`** (string) – Winner Team Name. Full name of the team that won the game.
  - **`winner_team_abbrev`** (string) – Winner Team Abbreviation. Three-letter abbreviation for the team that won the game (e.g., "NYR").
  - **`loser_team_name`** (string) – Loser Team Name. Full name of the team that lost the game.
  - **`loser_team_abbrev`** (string) – Loser Team Abbreviation. Three-letter abbreviation for the team that lost the game (e.g., "BOS").
  - **`overtime`** (string) – Overtime. Indicates whether the game went to overtime, and may include additional info such as the number of overtime periods (e.g., "OT", "2OT", or NULL if decided in regulation).

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_playoff_series_result_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_playoff_series_result_now/
```
<a name="league_playoff_series_result_{year}/game_id/{game_id}"></a>
### 5.2 Get playoff result by year and specific game
- **Endpoint:** `/league_playoff_series_result_{year}/game_id/{game_id}/`
- **Method:** GET
- **Description:** Table with results of playoff series games for a specific game. 
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
     - **`game_id`** (string) - Game ID. Unique identifier for each playoff game (e.g. "202008020VAN").
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) – Season ID. Unique identifier for the NHL season (e.g., 20212022).
  - **`game_id`** (string) – Game ID. Unique identifier for each playoff game.
  - **`round_name`** (string) – Round Name. The name or description of the playoff round (e.g., "Quarterfinals", "Stanley Cup Final").
  - **`game_number`** (string) – Game Number. The sequential number of the game within the series (e.g., "Game 5").
  - **`game_date`** (date) – Game Date. The date on which the playoff game was played (e.g., "2021-08-21").
  - **`away_team_name`** (string) – Away Team Name. Full name of the away (visiting) team.
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team.
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Three-letter abbreviation for the home team (e.g., "BOS").
  - **`away_team_score`** (integer) – Away Team Score. Number of goals scored by the away team in this game.
  - **`home_team_score`** (integer) – Home Team Score. Number of goals scored by the home team in this game.
  - **`winner_team_name`** (string) – Winner Team Name. Full name of the team that won the game.
  - **`winner_team_abbrev`** (string) – Winner Team Abbreviation. Three-letter abbreviation for the team that won the game.
  - **`loser_team_name`** (string) – Loser Team Name. Full name of the team that lost the game.
  - **`loser_team_abbrev`** (string) – Loser Team Abbreviation. Three-letter abbreviation for the team that lost the game.
  - **`overtime`** (string) – Overtime. Indicates whether the game went to overtime, and may include additional info such as the number of overtime periods (e.g., "OT", "2OT", or NULL if decided in regulation).

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_playoff_series_result_20212022/game_id/202205040EDM/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_playoff_series_result_now/game_id/202504200CAR/
```
<a name="league_playoff_series_result_{year}/game_date/{game_date}"></a>
### 5.3 Get playoff result by year and specific date
- **Endpoint:** `/league_playoff_series_result_{year}/game_date/{game_date}/`
- **Method:** GET
- **Description:** Table with results of playoff series games for a specific date.
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
     - **`game_date`** (date) - Game Date. The date on which the playoff game was played (e.g., "2021-08-21").
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) – Season ID. Unique identifier for the NHL season (e.g., 20212022).
  - **`game_id`** (string) – Game ID. Unique identifier for each playoff game.
  - **`round_name`** (string) – Round Name. The name or description of the playoff round (e.g., "Quarterfinals", "Stanley Cup Final").
  - **`game_number`** (string) – Game Number. The sequential number of the game within the series (e.g., "Game 5").
  - **`game_date`** (date) – Game Date. The date on which the playoff game was played (e.g., "2021-08-21").
  - **`away_team_name`** (string) – Away Team Name. Full name of the away (visiting) team.
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team.
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Three-letter abbreviation for the home team (e.g., "BOS").
  - **`away_team_score`** (integer) – Away Team Score. Number of goals scored by the away team in this game.
  - **`home_team_score`** (integer) – Home Team Score. Number of goals scored by the home team in this game.
  - **`winner_team_name`** (string) – Winner Team Name. Full name of the team that won the game.
  - **`winner_team_abbrev`** (string) – Winner Team Abbreviation. Three-letter abbreviation for the team that won the game.
  - **`loser_team_name`** (string) – Loser Team Name. Full name of the team that lost the game.
  - **`loser_team_abbrev`** (string) – Loser Team Abbreviation. Three-letter abbreviation for the team that lost the game.
  - **`overtime`** (string) – Overtime. Indicates whether the game went to overtime, and may include additional info such as the number of overtime periods (e.g., "OT", "2OT", or NULL if decided in regulation).

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_playoff_series_result_20212022/game_date/2022-05-04/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_playoff_series_result_now/game_date/2022-05-04/
```
<a name="playoff_schedule_{year}"></a>
### 5.4 Get playoff schedule by year
- **Endpoint:** `/playoff_schedule_{year}/`
- **Method:** GET
- **Description:** Table with schedule and results for all playoff games for the specified year. 
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`game_id`** (string) – Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`game_date`** (date) –  Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_time`** (string) – Game Time. Scheduled local start time of the game in 12-hour format; or null if unknown (e.g., "10:00 PM").
  - **`away_team_name`** (string) – Away Team Name. Full name of the visiting team (e.g., "Toronto Maple Leafs").
  - **`away_team_abbrev`** (string) –  Away Team Abbreviation. Official abbreviation (e.g., "TOR").
  - **`away_team_goals`** (integer) – Away Team Goals. Goals scored by away team; null if not played (e.g., 2).
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team (e.g., "Montreal Canadiens").
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Official abbreviation (e.g., "MTL").
  - **`home_team_goals`** (integer) –  Home Team Goals. Goals scored by home team; null if not played (e.g., 3).
  - **`overtime`** (string) –  Overtime or Shootout. "OT", "2OT", "SO" or null if decided in regulation.
  - **`attendance `** (integer) – Attendance. Number of spectators at the game; null if not available (e.g., 21047).
  - **`game_duration`** (string) – Game Duration. Length of game in hours and minutes "H:MM"; null if not played (e.g., "2:33").

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/playoff_schedule_{year}/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/playoff_schedule_now/
```
<a name="playoff_schedule_{year}/game_date/{game_date}"></a>
### 5.5 Get playoff schedule by year and specific date
- **Endpoint:** `/playoff_schedule_{year}/game_date/{game_date}`
- **Method:** GET
- **Description:** Table with schedule and results for all games played on a specific date within the chosen season.
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
     - **`game_date`** (date) - Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
- **Response:** JSON format
- **Schema table:**
  - **`game_id`** (string) – Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`game_date`** (date) –  Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_time`** (string) – Game Time. Scheduled local start time of the game in 12-hour format; or null if unknown (e.g., "10:00 PM").
  - **`away_team_name`** (string) – Away Team Name. Full name of the visiting team (e.g., "Toronto Maple Leafs").
  - **`away_team_abbrev`** (string) –  Away Team Abbreviation. Official abbreviation (e.g., "TOR").
  - **`away_team_goals`** (integer) – Away Team Goals. Goals scored by away team; null if not played (e.g., 2).
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team (e.g., "Montreal Canadiens").
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Official abbreviation (e.g., "MTL").
  - **`home_team_goals`** (integer) –  Home Team Goals. Goals scored by home team; null if not played (e.g., 3).
  - **`overtime`** (string) –  Overtime or Shootout. "OT", "2OT", "SO" or null if decided in regulation.
  - **`attendance `** (integer) – Attendance. Number of spectators at the game; null if not available (e.g., 21047).
  - **`game_duration`** (string) – Game Duration. Length of game in hours and minutes "H:MM"; null if not played (e.g., "2:33").

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/playoff_schedule_{year}/game_date/{game_date}/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/playoff_schedule_now/game_date/{game_date}/
```
<a name="playoff_schedule_{year}/game_id/{game_id}"></a>
### 5.6 Get playoff schedule by year and specific date
- **Endpoint:** `/playoff_schedule_{year}/game_id/{game_id}`
- **Method:** GET
- **Description:** Information about a specific game by its unique game ID.
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
     - **`game_id`** (string) - Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
- **Response:** JSON format
- **Schema table:**
  - **`game_id`** (string) – Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`game_date`** (date) –  Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_time`** (string) – Game Time. Scheduled local start time of the game in 12-hour format; or null if unknown (e.g., "10:00 PM").
  - **`away_team_name`** (string) – Away Team Name. Full name of the visiting team (e.g., "Toronto Maple Leafs").
  - **`away_team_abbrev`** (string) –  Away Team Abbreviation. Official abbreviation (e.g., "TOR").
  - **`away_team_goals`** (integer) – Away Team Goals. Goals scored by away team; null if not played (e.g., 2).
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team (e.g., "Montreal Canadiens").
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Official abbreviation (e.g., "MTL").
  - **`home_team_goals`** (integer) –  Home Team Goals. Goals scored by home team; null if not played (e.g., 3).
  - **`overtime`** (string) –  Overtime or Shootout. "OT", "2OT", "SO" or null if decided in regulation.
  - **`attendance `** (integer) – Attendance. Number of spectators at the game; null if not available (e.g., 21047).
  - **`game_duration`** (string) – Game Duration. Length of game in hours and minutes "H:MM"; null if not played (e.g., "2:33").

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/playoff_schedule_{year}/game_id/{game_id}/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/playoff_schedule_now/game_id/{game_id}/
```
<a name="playoff_schedule_{year}/team_abbrev/{team_abbrev}"></a>
### 5.7 Get playoff schedule by year and specific team
- **Endpoint:** `/playoff_schedule_{year}/team_abbrev/{team_abbrev}`
- **Method:** GET
- **Description:** Table with all games for a specific team in the selected season.
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
     - **`team_abbrev`** (string) - Team's official abbreviation (e.g., "TOR").
- **Response:** JSON format
- **Schema table:**
  - **`game_id`** (string) – Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`game_date`** (date) –  Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_time`** (string) – Game Time. Scheduled local start time of the game in 12-hour format; or null if unknown (e.g., "10:00 PM").
  - **`away_team_name`** (string) – Away Team Name. Full name of the visiting team (e.g., "Toronto Maple Leafs").
  - **`away_team_abbrev`** (string) –  Away Team Abbreviation. Official abbreviation (e.g., "TOR").
  - **`away_team_goals`** (integer) – Away Team Goals. Goals scored by away team; null if not played (e.g., 2).
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team (e.g., "Montreal Canadiens").
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Official abbreviation (e.g., "MTL").
  - **`home_team_goals`** (integer) –  Home Team Goals. Goals scored by home team; null if not played (e.g., 3).
  - **`overtime`** (string) –  Overtime or Shootout. "OT", "2OT", "SO" or null if decided in regulation.
  - **`attendance `** (integer) – Attendance. Number of spectators at the game; null if not available (e.g., 21047).
  - **`game_duration`** (string) – Game Duration. Length of game in hours and minutes "H:MM"; null if not played (e.g., "2:33").

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/playoff_schedule_{year}/team_abbrev/{team_abbrev}/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/playoff_schedule_now/team_abbrev/{team_abbrev}/
```
<a name="playoff_schedule_{year}/finished"></a>
### 5.8 Get playoff schedule by year and finished game
- **Endpoint:** `/playoff_schedule_{year}/finished`
- **Method:** GET
- **Description:** Table with all finished (concluded) playoff games in the selected season.
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`game_id`** (string) – Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`game_date`** (date) –  Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_time`** (string) – Game Time. Scheduled local start time of the game in 12-hour format; or null if unknown (e.g., "10:00 PM").
  - **`away_team_name`** (string) – Away Team Name. Full name of the visiting team (e.g., "Toronto Maple Leafs").
  - **`away_team_abbrev`** (string) –  Away Team Abbreviation. Official abbreviation (e.g., "TOR").
  - **`away_team_goals`** (integer) – Away Team Goals. Goals scored by away team; null if not played (e.g., 2).
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team (e.g., "Montreal Canadiens").
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Official abbreviation (e.g., "MTL").
  - **`home_team_goals`** (integer) –  Home Team Goals. Goals scored by home team; null if not played (e.g., 3).
  - **`overtime`** (string) –  Overtime or Shootout. "OT", "2OT", "SO" or null if decided in regulation.
  - **`attendance `** (integer) – Attendance. Number of spectators at the game; null if not available (e.g., 21047).
  - **`game_duration`** (string) – Game Duration. Length of game in hours and minutes "H:MM"; null if not played (e.g., "2:33").

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/playoff_schedule_{year}/finished/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/playoff_schedule_now/finished/
```
<a name="playoff_schedule_{year}/upcoming"></a>
### 5.9 Get playoff schedule by year and upcoming game
- **Endpoint:** `/playoff_schedule_{year}/upcoming`
- **Method:** GET
- **Description:** Table with all upcoming games in the selected season.
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`game_id`** (string) – Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`game_date`** (date) –  Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_time`** (string) – Game Time. Scheduled local start time of the game in 12-hour format; or null if unknown (e.g., "10:00 PM").
  - **`away_team_name`** (string) – Away Team Name. Full name of the visiting team (e.g., "Toronto Maple Leafs").
  - **`away_team_abbrev`** (string) –  Away Team Abbreviation. Official abbreviation (e.g., "TOR").
  - **`away_team_goals`** (integer) – Away Team Goals. Goals scored by away team; null if not played (e.g., 2).
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team (e.g., "Montreal Canadiens").
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Official abbreviation (e.g., "MTL").
  - **`home_team_goals`** (integer) –  Home Team Goals. Goals scored by home team; null if not played (e.g., 3).
  - **`overtime`** (string) –  Overtime or Shootout. "OT", "2OT", "SO" or null if decided in regulation.
  - **`attendance `** (integer) – Attendance. Number of spectators at the game; null if not available (e.g., 21047).
  - **`game_duration`** (string) – Game Duration. Length of game in hours and minutes "H:MM"; null if not played (e.g., "2:33").

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/playoff_schedule_{year}/upcoming/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/playoff_schedule_now/upcoming/
```
<a name="playoff_schedule_{year}/upcoming_day"></a>
### 5.10 Get playoff schedule by year and upcoming game for next day
- **Endpoint:** `/playoff_schedule_{year}/upcoming_day`
- **Method:** GET
- **Description:** Table with all games scheduled for the next day in the selected season. If today is 06/25/2025 and the next first games will start only on 10/25/2025, it will take the date for 10/25/2025, since these are the first available games.
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`game_id`** (string) – Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`game_date`** (date) –  Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_time`** (string) – Game Time. Scheduled local start time of the game in 12-hour format; or null if unknown (e.g., "10:00 PM").
  - **`away_team_name`** (string) – Away Team Name. Full name of the visiting team (e.g., "Toronto Maple Leafs").
  - **`away_team_abbrev`** (string) –  Away Team Abbreviation. Official abbreviation (e.g., "TOR").
  - **`away_team_goals`** (integer) – Away Team Goals. Goals scored by away team; null if not played (e.g., 2).
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team (e.g., "Montreal Canadiens").
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Official abbreviation (e.g., "MTL").
  - **`home_team_goals`** (integer) –  Home Team Goals. Goals scored by home team; null if not played (e.g., 3).
  - **`overtime`** (string) –  Overtime or Shootout. "OT", "2OT", "SO" or null if decided in regulation.
  - **`attendance `** (integer) – Attendance. Number of spectators at the game; null if not available (e.g., 21047).
  - **`game_duration`** (string) – Game Duration. Length of game in hours and minutes "H:MM"; null if not played (e.g., "2:33").

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/playoff_schedule_{year}/upcoming_day/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/playoff_schedule_now/upcoming_day/
```
<a name="playoff_schedule_{year}/upcoming_week"></a>
### 5.11 Get playoff schedule by year and upcoming game for next week
- **Endpoint:** `/playoff_schedule_{year}/upcoming_week`
- **Method:** GET
- **Description:** Table with all games scheduled for the next week in the selected season.
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`game_id`** (string) – Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`game_date`** (date) –  Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_time`** (string) – Game Time. Scheduled local start time of the game in 12-hour format; or null if unknown (e.g., "10:00 PM").
  - **`away_team_name`** (string) – Away Team Name. Full name of the visiting team (e.g., "Toronto Maple Leafs").
  - **`away_team_abbrev`** (string) –  Away Team Abbreviation. Official abbreviation (e.g., "TOR").
  - **`away_team_goals`** (integer) – Away Team Goals. Goals scored by away team; null if not played (e.g., 2).
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team (e.g., "Montreal Canadiens").
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Official abbreviation (e.g., "MTL").
  - **`home_team_goals`** (integer) –  Home Team Goals. Goals scored by home team; null if not played (e.g., 3).
  - **`overtime`** (string) –  Overtime or Shootout. "OT", "2OT", "SO" or null if decided in regulation.
  - **`attendance `** (integer) – Attendance. Number of spectators at the game; null if not available (e.g., 21047).
  - **`game_duration`** (string) – Game Duration. Length of game in hours and minutes "H:MM"; null if not played (e.g., "2:33").

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/playoff_schedule_{year}/upcoming_week/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/playoff_schedule_now/upcoming_week/
```
<a name="playoff_schedule_{year}/upcoming_month"></a>
### 5.12 Get playoff schedule by year and upcoming game for next month
- **Endpoint:** `/playoff_schedule_{year}/upcoming_month`
- **Method:** GET
- **Description:** Table with all games scheduled for the next month in the selected season.
- **Parameters:**
     - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`game_id`** (string) – Game ID. Unique identifier for the game within the season (e.g., "201301190NYI").
  - **`game_date`** (date) –  Game Date. Date the game was played or is scheduled "YYYY-MM-DD" (e.g., "2023-12-15").
  - **`game_time`** (string) – Game Time. Scheduled local start time of the game in 12-hour format; or null if unknown (e.g., "10:00 PM").
  - **`away_team_name`** (string) – Away Team Name. Full name of the visiting team (e.g., "Toronto Maple Leafs").
  - **`away_team_abbrev`** (string) –  Away Team Abbreviation. Official abbreviation (e.g., "TOR").
  - **`away_team_goals`** (integer) – Away Team Goals. Goals scored by away team; null if not played (e.g., 2).
  - **`away_team_abbrev`** (string) – Away Team Abbreviation. Three-letter abbreviation for the away team (e.g., "NYR").
  - **`home_team_name`** (string) – Home Team Name. Full name of the home team (e.g., "Montreal Canadiens").
  - **`home_team_abbrev`** (string) – Home Team Abbreviation. Official abbreviation (e.g., "MTL").
  - **`home_team_goals`** (integer) –  Home Team Goals. Goals scored by home team; null if not played (e.g., 3).
  - **`overtime`** (string) –  Overtime or Shootout. "OT", "2OT", "SO" or null if decided in regulation.
  - **`attendance `** (integer) – Attendance. Number of spectators at the game; null if not available (e.g., 21047).
  - **`game_duration`** (string) – Game Duration. Length of game in hours and minutes "H:MM"; null if not played (e.g., "2:33").

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/playoff_schedule_{year}/upcoming_month/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/playoff_schedule_now/upcoming_month/
```
