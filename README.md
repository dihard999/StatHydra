# :crab:CrashCrab | Sports API and Machine Learning for Match Prediction
**This application is a powerful API for sports analytics and match prediction, leveraging state-of-the-art machine learning algorithms. Designed for enthusiasts, analysts, and developers. With its robust and scalable architecture, the API offers seamless integration and real-time predictions, making it an essential tool for anyone seeking data-driven insights into the world of sports.**
> [!NOTE]
> **Development is only available for NHL, development of other sports is in progress....**  
> **The data starts from 2017. Of course, if most people need years earlier, we will consider this possibility.**
---
---
# NHL
1. [Base URL](#base-url)
2. [Player](#player)  
   2.1 [Get player leaders by year and all category](#league_leaders_{year})  
   2.2 [Get player leaders by year and specific category](#league_leaders_{year}/category/{leader_id_abbrev})  
   2.3 [Get player leaders by year and specific category and rank](#league_leaders_{year}/category/{leader_id_abbrev}/rank/{rank})  
   2.4 [Get player leaders by year and specific category and player ID](#league_leaders_{year}/category/{leader_id_abbrev}/player/{player_id})  
   2.5 [Get player leaders by year and specific category and team](#league_leaders_{year}/category/{leader_id_abbrev}/team/{team_abbrev})  
   2.6 [Get player leaders by year and specific rank](#league_leaders_{year}/rank/{rank})  
   2.7 [Get player leaders by year and specific rank and player ID](#league_leaders_{year}/rank/{rank}/player/{player_id})  
   2.8 [Get player leaders by year and specific rank and team](#league_leaders_{year}/rank/{rank}/team/{team_abbrev})  
   2.9 [Get player leaders by year and specific player ID](#league_leaders_{year}/player/{player_id})  
   2.10 [Get player leaders by year and specific team](#league_leaders_{year}/team/{team_abbrev})  
   2.11 [Get player leaders by year and specific team and player ID](#league_leaders_{year}/team/{team_abbrev}/player/{player_id})  
3. [Team](#team)  
   3.1 [Get all season teams statistics summary(except for the current season)](#team_all_season_summary)  
   3.2 [Get all season teams statistics summary by specific team(except for the current season)](#team_all_season_summary/{abbreviation})  
   3.3 [Get teams analytics 5 on 5 by year](#team_analytics_5_on_5_{year})  
   3.4 [Get teams analytics 5 on 5 by year and specific team](#team_analytics_5_on_5_{year}/{abbreviation})  
4. [Season](#season)  
   4.1 [Get summary statistic season by year](#season_summary_{year})  
   4.2 [Get summary statistic season by year and specific team](#season_summary_{year}/{abbreviation})  
   4.3 [Get detail statistic season by year](#season_statistics_{year})  
   4.4 [Get detail statistic season by year and specific team](#season_statistics_{year}/{abbreviation})  
   4.5 [Get league average by year](#league_average_{year})  
5. [Playoff](#playoff)  
   5.1 [Get playoff result by year](#league_playoff_series_result_{year})  
   5.2 [Get playoff result by year and specific game](#league_playoff_series_result_{year}/game/{game_id})  
   5.3 [Get playoff result by year and specific date](#league_playoff_series_result_{year}/date/{game_date})  
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
### 2.1 Get player leaders by year and all category
- **Endpoint:** `/league_leaders_{year}/`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and all category.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`leader_id`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`leader_id_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:
    
```  
╔════════════════════════════════════════╦══════════════╗  
║ Category                               ║ Short code   ║  
╠════════════════════════════════════════╬══════════════╣  
║ Assists                                ║ A            ║  
║ Assists Per Game                       ║ APG          ║  
║ Defensive Point Shares                 ║ DPS          ║  
║ Even Strength Goals                    ║ EVSG         ║  
║ Expected +/-                           ║ XPM          ║  
║ Game-Winning Goals                     ║ GWG          ║  
║ Games Played (Goalie)                  ║ GPG          ║  
║ Goalie Point Shares                    ║ GPS          ║  
║ Goals                                  ║ G            ║  
║ Goals Against                          ║ GA           ║  
║ Goals Against Average                  ║ GAA          ║  
║ Goals Allowed Adjusted                 ║ GAAJ         ║  
║ Goals Created                          ║ GCR          ║  
║ Goals Created Per Game                 ║ GCPG         ║  
║ Goals Per Game                         ║ GPGM         ║  
║ Goals Saved Above Average              ║ GSAA         ║  
║ Hat Tricks                             ║ HTR          ║  
║ Losses                                 ║ L            ║  
║ Minutes                                ║ MIN          ║  
║ Offensive Point Shares                 ║ OPS          ║  
║ Penalties in Minutes                   ║ PIM          ║  
║ Plus/Minus                             ║ PLM          ║  
║ Point Shares                           ║ PTS          ║  
║ Points                                 ║ P            ║  
║ Points Per Game                        ║ PPG          ║  
║ Power Play Goals                       ║ PPGL         ║  
║ Power Play Goals On-Ice Against        ║ PGAI         ║  
║ Power Play Goals On-Ice For            ║ PGFI         ║  
║ Save Percentage                        ║ SVP          ║  
║ Saves                                  ║ SAV          ║  
║ Shooting Percentage                    ║ SHP          ║  
║ Short-Handed Goals                     ║ SHG          ║  
║ Shots                                  ║ S            ║  
║ Shots Against                          ║ SAG          ║  
║ Shutouts                               ║ SHO          ║  
║ Ties plus OT/SO Losses                 ║ TOL          ║  
║ Total Goals On-Ice Against             ║ TGAI         ║  
║ Total Goals On-Ice For                 ║ TGFI         ║  
║ Wins                                   ║ W            ║  
╚════════════════════════════════════════╩══════════════╝  
```  
##### Example using by specific year
```cURL Config
http://crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/
```
<a name="league_leaders_{year}/category/{leader_id_abbrev}"></a>
### 2.2 Get player leaders by year and specific category
- **Endpoint:** `/league_leaders_{year}/category/{leader_id_abbrev}`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and specific category.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{leader_id_abbrev}`** (string) - Short abbreviation of categories.
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`leader_id`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`leader_id_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:  
```  
╔════════════════════════════════════════╦══════════════╗  
║ Category                               ║ Short code   ║  
╠════════════════════════════════════════╬══════════════╣  
║ Assists                                ║ A            ║  
║ Assists Per Game                       ║ APG          ║  
║ Defensive Point Shares                 ║ DPS          ║  
║ Even Strength Goals                    ║ EVSG         ║  
║ Expected +/-                           ║ XPM          ║  
║ Game-Winning Goals                     ║ GWG          ║  
║ Games Played (Goalie)                  ║ GPG          ║  
║ Goalie Point Shares                    ║ GPS          ║  
║ Goals                                  ║ G            ║  
║ Goals Against                          ║ GA           ║  
║ Goals Against Average                  ║ GAA          ║  
║ Goals Allowed Adjusted                 ║ GAAJ         ║  
║ Goals Created                          ║ GCR          ║  
║ Goals Created Per Game                 ║ GCPG         ║  
║ Goals Per Game                         ║ GPGM         ║  
║ Goals Saved Above Average              ║ GSAA         ║  
║ Hat Tricks                             ║ HTR          ║  
║ Losses                                 ║ L            ║  
║ Minutes                                ║ MIN          ║  
║ Offensive Point Shares                 ║ OPS          ║  
║ Penalties in Minutes                   ║ PIM          ║  
║ Plus/Minus                             ║ PLM          ║  
║ Point Shares                           ║ PTS          ║  
║ Points                                 ║ P            ║  
║ Points Per Game                        ║ PPG          ║  
║ Power Play Goals                       ║ PPGL         ║  
║ Power Play Goals On-Ice Against        ║ PGAI         ║  
║ Power Play Goals On-Ice For            ║ PGFI         ║  
║ Save Percentage                        ║ SVP          ║  
║ Saves                                  ║ SAV          ║  
║ Shooting Percentage                    ║ SHP          ║  
║ Short-Handed Goals                     ║ SHG          ║  
║ Shots                                  ║ S            ║  
║ Shots Against                          ║ SAG          ║  
║ Shutouts                               ║ SHO          ║  
║ Ties plus OT/SO Losses                 ║ TOL          ║  
║ Total Goals On-Ice Against             ║ TGAI         ║  
║ Total Goals On-Ice For                 ║ TGFI         ║  
║ Wins                                   ║ W            ║  
╚════════════════════════════════════════╩══════════════╝  
```  

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/category/GPS/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/category/GPS/
```
<a name="league_leaders_{year}/category/{leader_id_abbrev}/rank/{rank}"></a>
### 2.3 Get player leaders by year and specific category and rank
- **Endpoint:** `/league_leaders_{year}/category/{leader_id_abbrev}/rank/{rank}`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and specific category and rank.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{leader_id_abbrev}`** (string) - Short abbreviation of categories.
   - **`{rank}`** (string) - Rank in the leaderboard, first place is the best.
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`leader_id`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`leader_id_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:  
```  
╔════════════════════════════════════════╦══════════════╗  
║ Category                               ║ Short code   ║  
╠════════════════════════════════════════╬══════════════╣  
║ Assists                                ║ A            ║  
║ Assists Per Game                       ║ APG          ║  
║ Defensive Point Shares                 ║ DPS          ║  
║ Even Strength Goals                    ║ EVSG         ║  
║ Expected +/-                           ║ XPM          ║  
║ Game-Winning Goals                     ║ GWG          ║  
║ Games Played (Goalie)                  ║ GPG          ║  
║ Goalie Point Shares                    ║ GPS          ║  
║ Goals                                  ║ G            ║  
║ Goals Against                          ║ GA           ║  
║ Goals Against Average                  ║ GAA          ║  
║ Goals Allowed Adjusted                 ║ GAAJ         ║  
║ Goals Created                          ║ GCR          ║  
║ Goals Created Per Game                 ║ GCPG         ║  
║ Goals Per Game                         ║ GPGM         ║  
║ Goals Saved Above Average              ║ GSAA         ║  
║ Hat Tricks                             ║ HTR          ║  
║ Losses                                 ║ L            ║  
║ Minutes                                ║ MIN          ║  
║ Offensive Point Shares                 ║ OPS          ║  
║ Penalties in Minutes                   ║ PIM          ║  
║ Plus/Minus                             ║ PLM          ║  
║ Point Shares                           ║ PTS          ║  
║ Points                                 ║ P            ║  
║ Points Per Game                        ║ PPG          ║  
║ Power Play Goals                       ║ PPGL         ║  
║ Power Play Goals On-Ice Against        ║ PGAI         ║  
║ Power Play Goals On-Ice For            ║ PGFI         ║  
║ Save Percentage                        ║ SVP          ║  
║ Saves                                  ║ SAV          ║  
║ Shooting Percentage                    ║ SHP          ║  
║ Short-Handed Goals                     ║ SHG          ║  
║ Shots                                  ║ S            ║  
║ Shots Against                          ║ SAG          ║  
║ Shutouts                               ║ SHO          ║  
║ Ties plus OT/SO Losses                 ║ TOL          ║  
║ Total Goals On-Ice Against             ║ TGAI         ║  
║ Total Goals On-Ice For                 ║ TGFI         ║  
║ Wins                                   ║ W            ║  
╚════════════════════════════════════════╩══════════════╝  
```  

##### Example by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/category/GPS/rank/3/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/category/GPS/rank/3/
```
<a name="league_leaders_{year}/category/{leader_id_abbrev}/player/{player_id}"></a>
### 2.4 Get player leaders by year and specific category and player ID
- **Endpoint:** `/league_leaders_{year}/category/{leader_id_abbrev}/player/{player_id}`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and specific category and player ID.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{leader_id_abbrev}`** (string) - Short abbreviation of categories.
   - **`{player_id}`** (string) - Unique identifier for each player, contains letters and numbers.
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`leader_id`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`leader_id_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:  
```  
╔════════════════════════════════════════╦══════════════╗  
║ Category                               ║ Short code   ║  
╠════════════════════════════════════════╬══════════════╣  
║ Assists                                ║ A            ║  
║ Assists Per Game                       ║ APG          ║  
║ Defensive Point Shares                 ║ DPS          ║  
║ Even Strength Goals                    ║ EVSG         ║  
║ Expected +/-                           ║ XPM          ║  
║ Game-Winning Goals                     ║ GWG          ║  
║ Games Played (Goalie)                  ║ GPG          ║  
║ Goalie Point Shares                    ║ GPS          ║  
║ Goals                                  ║ G            ║  
║ Goals Against                          ║ GA           ║  
║ Goals Against Average                  ║ GAA          ║  
║ Goals Allowed Adjusted                 ║ GAAJ         ║  
║ Goals Created                          ║ GCR          ║  
║ Goals Created Per Game                 ║ GCPG         ║  
║ Goals Per Game                         ║ GPGM         ║  
║ Goals Saved Above Average              ║ GSAA         ║  
║ Hat Tricks                             ║ HTR          ║  
║ Losses                                 ║ L            ║  
║ Minutes                                ║ MIN          ║  
║ Offensive Point Shares                 ║ OPS          ║  
║ Penalties in Minutes                   ║ PIM          ║  
║ Plus/Minus                             ║ PLM          ║  
║ Point Shares                           ║ PTS          ║  
║ Points                                 ║ P            ║  
║ Points Per Game                        ║ PPG          ║  
║ Power Play Goals                       ║ PPGL         ║  
║ Power Play Goals On-Ice Against        ║ PGAI         ║  
║ Power Play Goals On-Ice For            ║ PGFI         ║  
║ Save Percentage                        ║ SVP          ║  
║ Saves                                  ║ SAV          ║  
║ Shooting Percentage                    ║ SHP          ║  
║ Short-Handed Goals                     ║ SHG          ║  
║ Shots                                  ║ S            ║  
║ Shots Against                          ║ SAG          ║  
║ Shutouts                               ║ SHO          ║  
║ Ties plus OT/SO Losses                 ║ TOL          ║  
║ Total Goals On-Ice Against             ║ TGAI         ║  
║ Total Goals On-Ice For                 ║ TGFI         ║  
║ Wins                                   ║ W            ║  
╚════════════════════════════════════════╩══════════════╝  
```  

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/category/GPS/player/vasilan02/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/category/GPS/player/vasilan02/
```
<a name="league_leaders_{year}/category/{leader_id_abbrev}/team/{team_abbrev}"></a>
### 2.5 Get player leaders by year and specific category and team
- **Endpoint:** `/league_leaders_{year}/category/{leader_id_abbrev}/team/{team_abbrev}`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and specific category and team.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{leader_id_abbrev}`** (string) - Short abbreviation of categories.
   - **`{team_abbrev}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`leader_id`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`leader_id_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:  
```  
╔════════════════════════════════════════╦══════════════╗  
║ Category                               ║ Short code   ║  
╠════════════════════════════════════════╬══════════════╣  
║ Assists                                ║ A            ║  
║ Assists Per Game                       ║ APG          ║  
║ Defensive Point Shares                 ║ DPS          ║  
║ Even Strength Goals                    ║ EVSG         ║  
║ Expected +/-                           ║ XPM          ║  
║ Game-Winning Goals                     ║ GWG          ║  
║ Games Played (Goalie)                  ║ GPG          ║  
║ Goalie Point Shares                    ║ GPS          ║  
║ Goals                                  ║ G            ║  
║ Goals Against                          ║ GA           ║  
║ Goals Against Average                  ║ GAA          ║  
║ Goals Allowed Adjusted                 ║ GAAJ         ║  
║ Goals Created                          ║ GCR          ║  
║ Goals Created Per Game                 ║ GCPG         ║  
║ Goals Per Game                         ║ GPGM         ║  
║ Goals Saved Above Average              ║ GSAA         ║  
║ Hat Tricks                             ║ HTR          ║  
║ Losses                                 ║ L            ║  
║ Minutes                                ║ MIN          ║  
║ Offensive Point Shares                 ║ OPS          ║  
║ Penalties in Minutes                   ║ PIM          ║  
║ Plus/Minus                             ║ PLM          ║  
║ Point Shares                           ║ PTS          ║  
║ Points                                 ║ P            ║  
║ Points Per Game                        ║ PPG          ║  
║ Power Play Goals                       ║ PPGL         ║  
║ Power Play Goals On-Ice Against        ║ PGAI         ║  
║ Power Play Goals On-Ice For            ║ PGFI         ║  
║ Save Percentage                        ║ SVP          ║  
║ Saves                                  ║ SAV          ║  
║ Shooting Percentage                    ║ SHP          ║  
║ Short-Handed Goals                     ║ SHG          ║  
║ Shots                                  ║ S            ║  
║ Shots Against                          ║ SAG          ║  
║ Shutouts                               ║ SHO          ║  
║ Ties plus OT/SO Losses                 ║ TOL          ║  
║ Total Goals On-Ice Against             ║ TGAI         ║  
║ Total Goals On-Ice For                 ║ TGFI         ║  
║ Wins                                   ║ W            ║  
╚════════════════════════════════════════╩══════════════╝  
```  

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/category/GPS/team/TBL/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/category/GPS/team/TBL/
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
  - **`leader_id`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`leader_id_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:  
```  
╔════════════════════════════════════════╦══════════════╗  
║ Category                               ║ Short code   ║  
╠════════════════════════════════════════╬══════════════╣  
║ Assists                                ║ A            ║  
║ Assists Per Game                       ║ APG          ║  
║ Defensive Point Shares                 ║ DPS          ║  
║ Even Strength Goals                    ║ EVSG         ║  
║ Expected +/-                           ║ XPM          ║  
║ Game-Winning Goals                     ║ GWG          ║  
║ Games Played (Goalie)                  ║ GPG          ║  
║ Goalie Point Shares                    ║ GPS          ║  
║ Goals                                  ║ G            ║  
║ Goals Against                          ║ GA           ║  
║ Goals Against Average                  ║ GAA          ║  
║ Goals Allowed Adjusted                 ║ GAAJ         ║  
║ Goals Created                          ║ GCR          ║  
║ Goals Created Per Game                 ║ GCPG         ║  
║ Goals Per Game                         ║ GPGM         ║  
║ Goals Saved Above Average              ║ GSAA         ║  
║ Hat Tricks                             ║ HTR          ║  
║ Losses                                 ║ L            ║  
║ Minutes                                ║ MIN          ║  
║ Offensive Point Shares                 ║ OPS          ║  
║ Penalties in Minutes                   ║ PIM          ║  
║ Plus/Minus                             ║ PLM          ║  
║ Point Shares                           ║ PTS          ║  
║ Points                                 ║ P            ║  
║ Points Per Game                        ║ PPG          ║  
║ Power Play Goals                       ║ PPGL         ║  
║ Power Play Goals On-Ice Against        ║ PGAI         ║  
║ Power Play Goals On-Ice For            ║ PGFI         ║  
║ Save Percentage                        ║ SVP          ║  
║ Saves                                  ║ SAV          ║  
║ Shooting Percentage                    ║ SHP          ║  
║ Short-Handed Goals                     ║ SHG          ║  
║ Shots                                  ║ S            ║  
║ Shots Against                          ║ SAG          ║  
║ Shutouts                               ║ SHO          ║  
║ Ties plus OT/SO Losses                 ║ TOL          ║  
║ Total Goals On-Ice Against             ║ TGAI         ║  
║ Total Goals On-Ice For                 ║ TGFI         ║  
║ Wins                                   ║ W            ║  
╚════════════════════════════════════════╩══════════════╝  
```  

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/rank/3/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/rank/3/
```
<a name="league_leaders_{year}/rank/{rank}/player/{player_id}"></a>
### 2.7 Get player leaders by year and specific rank and player ID
- **Endpoint:** `/league_leaders_{year}/rank/{rank}/player/{player_id}`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and specific rank and player ID.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{rank}`** (integer) - Rank in the leaderboard, first place is the best.
   - **`{player_id}`** (string) - Unique identifier for each player, contains letters and numbers.
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`leader_id`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`leader_id_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:  
```  
╔════════════════════════════════════════╦══════════════╗  
║ Category                               ║ Short code   ║  
╠════════════════════════════════════════╬══════════════╣  
║ Assists                                ║ A            ║  
║ Assists Per Game                       ║ APG          ║  
║ Defensive Point Shares                 ║ DPS          ║  
║ Even Strength Goals                    ║ EVSG         ║  
║ Expected +/-                           ║ XPM          ║  
║ Game-Winning Goals                     ║ GWG          ║  
║ Games Played (Goalie)                  ║ GPG          ║  
║ Goalie Point Shares                    ║ GPS          ║  
║ Goals                                  ║ G            ║  
║ Goals Against                          ║ GA           ║  
║ Goals Against Average                  ║ GAA          ║  
║ Goals Allowed Adjusted                 ║ GAAJ         ║  
║ Goals Created                          ║ GCR          ║  
║ Goals Created Per Game                 ║ GCPG         ║  
║ Goals Per Game                         ║ GPGM         ║  
║ Goals Saved Above Average              ║ GSAA         ║  
║ Hat Tricks                             ║ HTR          ║  
║ Losses                                 ║ L            ║  
║ Minutes                                ║ MIN          ║  
║ Offensive Point Shares                 ║ OPS          ║  
║ Penalties in Minutes                   ║ PIM          ║  
║ Plus/Minus                             ║ PLM          ║  
║ Point Shares                           ║ PTS          ║  
║ Points                                 ║ P            ║  
║ Points Per Game                        ║ PPG          ║  
║ Power Play Goals                       ║ PPGL         ║  
║ Power Play Goals On-Ice Against        ║ PGAI         ║  
║ Power Play Goals On-Ice For            ║ PGFI         ║  
║ Save Percentage                        ║ SVP          ║  
║ Saves                                  ║ SAV          ║  
║ Shooting Percentage                    ║ SHP          ║  
║ Short-Handed Goals                     ║ SHG          ║  
║ Shots                                  ║ S            ║  
║ Shots Against                          ║ SAG          ║  
║ Shutouts                               ║ SHO          ║  
║ Ties plus OT/SO Losses                 ║ TOL          ║  
║ Total Goals On-Ice Against             ║ TGAI         ║  
║ Total Goals On-Ice For                 ║ TGFI         ║  
║ Wins                                   ║ W            ║  
╚════════════════════════════════════════╩══════════════╝  
```  

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/rank/3/player/marksja02/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/rank/3/player/marksja02/
```
<a name="league_leaders_{year}/rank/{rank}/team/{team_abbrev}"></a>
### 2.8 Get player leaders by year and specific rank and team
- **Endpoint:** `/league_leaders_{year}/rank/{rank}/team/{team_abbrev}`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and specific rank and team.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{rank}`** (integer) - Rank in the leaderboard, first place is the best.
   - **`{team_abbrev}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`leader_id`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`leader_id_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:  
```  
╔════════════════════════════════════════╦══════════════╗  
║ Category                               ║ Short code   ║  
╠════════════════════════════════════════╬══════════════╣  
║ Assists                                ║ A            ║  
║ Assists Per Game                       ║ APG          ║  
║ Defensive Point Shares                 ║ DPS          ║  
║ Even Strength Goals                    ║ EVSG         ║  
║ Expected +/-                           ║ XPM          ║  
║ Game-Winning Goals                     ║ GWG          ║  
║ Games Played (Goalie)                  ║ GPG          ║  
║ Goalie Point Shares                    ║ GPS          ║  
║ Goals                                  ║ G            ║  
║ Goals Against                          ║ GA           ║  
║ Goals Against Average                  ║ GAA          ║  
║ Goals Allowed Adjusted                 ║ GAAJ         ║  
║ Goals Created                          ║ GCR          ║  
║ Goals Created Per Game                 ║ GCPG         ║  
║ Goals Per Game                         ║ GPGM         ║  
║ Goals Saved Above Average              ║ GSAA         ║  
║ Hat Tricks                             ║ HTR          ║  
║ Losses                                 ║ L            ║  
║ Minutes                                ║ MIN          ║  
║ Offensive Point Shares                 ║ OPS          ║  
║ Penalties in Minutes                   ║ PIM          ║  
║ Plus/Minus                             ║ PLM          ║  
║ Point Shares                           ║ PTS          ║  
║ Points                                 ║ P            ║  
║ Points Per Game                        ║ PPG          ║  
║ Power Play Goals                       ║ PPGL         ║  
║ Power Play Goals On-Ice Against        ║ PGAI         ║  
║ Power Play Goals On-Ice For            ║ PGFI         ║  
║ Save Percentage                        ║ SVP          ║  
║ Saves                                  ║ SAV          ║  
║ Shooting Percentage                    ║ SHP          ║  
║ Short-Handed Goals                     ║ SHG          ║  
║ Shots                                  ║ S            ║  
║ Shots Against                          ║ SAG          ║  
║ Shutouts                               ║ SHO          ║  
║ Ties plus OT/SO Losses                 ║ TOL          ║  
║ Total Goals On-Ice Against             ║ TGAI         ║  
║ Total Goals On-Ice For                 ║ TGFI         ║  
║ Wins                                   ║ W            ║  
╚════════════════════════════════════════╩══════════════╝  
```  

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/rank/3/team/TBL/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/rank/3/team/TBL/
```
<a name="league_leaders_{year}/player/{player_id}"></a>
### 2.9 Get player leaders by year and specific player ID
- **Endpoint:** `/league_leaders_{year}/player/{player_id}`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and specific player ID.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{player_id}`** (string) - Unique identifier for each player, contains letters and numbers.
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`leader_id`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`leader_id_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:  
```  
╔════════════════════════════════════════╦══════════════╗  
║ Category                               ║ Short code   ║  
╠════════════════════════════════════════╬══════════════╣  
║ Assists                                ║ A            ║  
║ Assists Per Game                       ║ APG          ║  
║ Defensive Point Shares                 ║ DPS          ║  
║ Even Strength Goals                    ║ EVSG         ║  
║ Expected +/-                           ║ XPM          ║  
║ Game-Winning Goals                     ║ GWG          ║  
║ Games Played (Goalie)                  ║ GPG          ║  
║ Goalie Point Shares                    ║ GPS          ║  
║ Goals                                  ║ G            ║  
║ Goals Against                          ║ GA           ║  
║ Goals Against Average                  ║ GAA          ║  
║ Goals Allowed Adjusted                 ║ GAAJ         ║  
║ Goals Created                          ║ GCR          ║  
║ Goals Created Per Game                 ║ GCPG         ║  
║ Goals Per Game                         ║ GPGM         ║  
║ Goals Saved Above Average              ║ GSAA         ║  
║ Hat Tricks                             ║ HTR          ║  
║ Losses                                 ║ L            ║  
║ Minutes                                ║ MIN          ║  
║ Offensive Point Shares                 ║ OPS          ║  
║ Penalties in Minutes                   ║ PIM          ║  
║ Plus/Minus                             ║ PLM          ║  
║ Point Shares                           ║ PTS          ║  
║ Points                                 ║ P            ║  
║ Points Per Game                        ║ PPG          ║  
║ Power Play Goals                       ║ PPGL         ║  
║ Power Play Goals On-Ice Against        ║ PGAI         ║  
║ Power Play Goals On-Ice For            ║ PGFI         ║  
║ Save Percentage                        ║ SVP          ║  
║ Saves                                  ║ SAV          ║  
║ Shooting Percentage                    ║ SHP          ║  
║ Short-Handed Goals                     ║ SHG          ║  
║ Shots                                  ║ S            ║  
║ Shots Against                          ║ SAG          ║  
║ Shutouts                               ║ SHO          ║  
║ Ties plus OT/SO Losses                 ║ TOL          ║  
║ Total Goals On-Ice Against             ║ TGAI         ║  
║ Total Goals On-Ice For                 ║ TGFI         ║  
║ Wins                                   ║ W            ║  
╚════════════════════════════════════════╩══════════════╝  
```  

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/player/kreidch01/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/player/kreidch01/
```
<a name="league_leaders_{year}/team/{team_abbrev}"></a>
### 2.10 Get player leaders by year and specific team
- **Endpoint:** `/league_leaders_{year}/team/{team_abbrev}`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and specific team.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{team_abbrev}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`leader_id`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`leader_id_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:  
```  
╔════════════════════════════════════════╦══════════════╗  
║ Category                               ║ Short code   ║  
╠════════════════════════════════════════╬══════════════╣  
║ Assists                                ║ A            ║  
║ Assists Per Game                       ║ APG          ║  
║ Defensive Point Shares                 ║ DPS          ║  
║ Even Strength Goals                    ║ EVSG         ║  
║ Expected +/-                           ║ XPM          ║  
║ Game-Winning Goals                     ║ GWG          ║  
║ Games Played (Goalie)                  ║ GPG          ║  
║ Goalie Point Shares                    ║ GPS          ║  
║ Goals                                  ║ G            ║  
║ Goals Against                          ║ GA           ║  
║ Goals Against Average                  ║ GAA          ║  
║ Goals Allowed Adjusted                 ║ GAAJ         ║  
║ Goals Created                          ║ GCR          ║  
║ Goals Created Per Game                 ║ GCPG         ║  
║ Goals Per Game                         ║ GPGM         ║  
║ Goals Saved Above Average              ║ GSAA         ║  
║ Hat Tricks                             ║ HTR          ║  
║ Losses                                 ║ L            ║  
║ Minutes                                ║ MIN          ║  
║ Offensive Point Shares                 ║ OPS          ║  
║ Penalties in Minutes                   ║ PIM          ║  
║ Plus/Minus                             ║ PLM          ║  
║ Point Shares                           ║ PTS          ║  
║ Points                                 ║ P            ║  
║ Points Per Game                        ║ PPG          ║  
║ Power Play Goals                       ║ PPGL         ║  
║ Power Play Goals On-Ice Against        ║ PGAI         ║  
║ Power Play Goals On-Ice For            ║ PGFI         ║  
║ Save Percentage                        ║ SVP          ║  
║ Saves                                  ║ SAV          ║  
║ Shooting Percentage                    ║ SHP          ║  
║ Short-Handed Goals                     ║ SHG          ║  
║ Shots                                  ║ S            ║  
║ Shots Against                          ║ SAG          ║  
║ Shutouts                               ║ SHO          ║  
║ Ties plus OT/SO Losses                 ║ TOL          ║  
║ Total Goals On-Ice Against             ║ TGAI         ║  
║ Total Goals On-Ice For                 ║ TGFI         ║  
║ Wins                                   ║ W            ║  
╚════════════════════════════════════════╩══════════════╝  
```  

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/team/TOR/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/team/TOR/
```
<a name="league_leaders_{year}/team/{team_abbrev}/player/{player_id}"></a>
### 2.11 Get player leaders by year and specific team and player ID
- **Endpoint:** `/league_leaders_{year}/team/{team_abbrev}/player/{player_id}`
- **Method:** GET
- **Description:** Contains statistics of leading players (league leaders) by year and specific team and player ID.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{team_abbrev}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
   - **`{player_id}`** (string) - Unique identifier for each player, contains letters and numbers.
- **Response:** JSON format
- **Schema table:**
  - **`season_id`** (integer) - Unique identifier for the sports season.
  - **`leader_id`** (string) - Category by which the indicators are compared (e.g., "Assists", "Defensive Point Shares").
  - **`rank`** (integer) - Rank in the leaderboard, first place is the best.
  - **`player`** (string) - Player's full name.
  - **`player_id`** (string) - Unique identifier for each player, contains letters and numbers.
  - **`team_abbrev`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`score`** (number, decimal) - The number of points can be both whole and fractional numbers.
  - **`leader_id_abbrev`** (string) - Short abbreviation of categories (e.g., "Assists" - "A"). Table short code:  
```  
╔════════════════════════════════════════╦══════════════╗  
║ Category                               ║ Short code   ║  
╠════════════════════════════════════════╬══════════════╣  
║ Assists                                ║ A            ║  
║ Assists Per Game                       ║ APG          ║  
║ Defensive Point Shares                 ║ DPS          ║  
║ Even Strength Goals                    ║ EVSG         ║  
║ Expected +/-                           ║ XPM          ║  
║ Game-Winning Goals                     ║ GWG          ║  
║ Games Played (Goalie)                  ║ GPG          ║  
║ Goalie Point Shares                    ║ GPS          ║  
║ Goals                                  ║ G            ║  
║ Goals Against                          ║ GA           ║  
║ Goals Against Average                  ║ GAA          ║  
║ Goals Allowed Adjusted                 ║ GAAJ         ║  
║ Goals Created                          ║ GCR          ║  
║ Goals Created Per Game                 ║ GCPG         ║  
║ Goals Per Game                         ║ GPGM         ║  
║ Goals Saved Above Average              ║ GSAA         ║  
║ Hat Tricks                             ║ HTR          ║  
║ Losses                                 ║ L            ║  
║ Minutes                                ║ MIN          ║  
║ Offensive Point Shares                 ║ OPS          ║  
║ Penalties in Minutes                   ║ PIM          ║  
║ Plus/Minus                             ║ PLM          ║  
║ Point Shares                           ║ PTS          ║  
║ Points                                 ║ P            ║  
║ Points Per Game                        ║ PPG          ║  
║ Power Play Goals                       ║ PPGL         ║  
║ Power Play Goals On-Ice Against        ║ PGAI         ║  
║ Power Play Goals On-Ice For            ║ PGFI         ║  
║ Save Percentage                        ║ SVP          ║  
║ Saves                                  ║ SAV          ║  
║ Shooting Percentage                    ║ SHP          ║  
║ Short-Handed Goals                     ║ SHG          ║  
║ Shots                                  ║ S            ║  
║ Shots Against                          ║ SAG          ║  
║ Shutouts                               ║ SHO          ║  
║ Ties plus OT/SO Losses                 ║ TOL          ║  
║ Total Goals On-Ice Against             ║ TGAI         ║  
║ Total Goals On-Ice For                 ║ TGFI         ║  
║ Wins                                   ║ W            ║  
╚════════════════════════════════════════╩══════════════╝  
```  

##### Example using by specific year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_20212022/team/TOR/player/matthau01/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_leaders_now/team/TOR/player/matthau01/
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
  - **`abbreviation`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
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
<a name="team_all_season_summary/{abbreviation}"></a>
### 3.2 Get all season teams statistics summary by specific team(except for the current season)
- **Endpoint:** `/team_all_season_summary/{abbreviation}`
- **Method:** GET
- **Description:** Retrieves aggregated statistics for all teams across all seasons they participated in the NHL.
- **Parameters:**
   - **`{abbreviation}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`team_name`** (string) - Full team name. The name of the NHL team.
  - **`abbreviation`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
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
crashcrab.ddns.net/{YOUR_API_KEY}/team_all_season_summary/TOR/
```
<a name="team_analytics_5_on_5_{year}"></a>
### 3.3 Get teams analytics 5 on 5 by year
- **Endpoint:** `/team_analytics_5_on_5_{year}/`
- **Method:** GET
- **Description:** Table presents advanced statistics for NHL teams , focusing on 5-on-5 play for specific season.
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`ranker`** (integer) - Rank. The position of the team in the ranking based on their performance metrics.
  - **`team_name`** (string) - Team Name. The name of the NHL team.
  - **`abbreviation`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
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
<a name="team_analytics_5_on_5_{year}/{abbreviation}"></a>
### 3.4 Get teams analytics 5 on 5 by year and specific team
- **Endpoint:** `/team_analytics_5_on_5_{year}/{abbreviation}/`
- **Method:** GET
- **Description:** Table presents advanced statistics for NHL teams , focusing on 5-on-5 play of a specific team for specific season
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{abbreviation}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`ranker`** (integer) - Rank. The position of the team in the ranking based on their performance metrics.
  - **`team_name`** (string) - Team Name. The name of the NHL team.
  - **`abbreviation`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
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
crashcrab.ddns.net/{YOUR_API_KEY}/team_analytics_5_on_5_20212022/TOR/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/team_analytics_5_on_5_now/TOR/
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
  - **`abbreviation`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
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
<a name="season_summary_{year}/{abbreviation}"></a>
### 4.2 Get summary statistic season by year and specific team 
- **Endpoint:** `/season_summary_{year}/{abbreviation}`
- **Method:** GET
- **Description:** Get summary statistics for a specific team for a specific season year
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{abbreviation}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`team_name`** (string) - Full team name. The name of the NHL team.
  - **`abbreviation`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
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
crashcrab.ddns.net/{YOUR_API_KEY}/season_summary_20212022/TOR/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/season_summary_now/TOR/
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
  - **`ranker`** (integer) - Rank. The ranking of the team in the league based on their performance. A lower number (e.g., 1) indicates a higher-ranked team.
  - **`team_name`** (string) - Full team name. The name of the NHL team.
  - **`abbreviation`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
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
<a name="season_statistics_{year}/{abbreviation}"></a>
### 4.4 Get detail statistic season by year and specific team
- **Endpoint:** `/season_statistics_{year}/{abbreviation}/`
- **Method:** GET
- **Description:** Detail statistics of a specific team for specific season
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{abbreviation}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`ranker`** (integer) - Rank. The ranking of the team in the league based on their performance. A lower number (e.g., 1) indicates a higher-ranked team.
  - **`team_name`** (string) - Full team name. The name of the NHL team.
  - **`abbreviation`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
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
crashcrab.ddns.net/{YOUR_API_KEY}/season_statistics_20212022/TOR/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/season_statistics_now/TOR/
```
<a name="league_average_{year}"></a>
### 4.5 Get league average by year
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
<a name="league_playoff_series_result_{year}/game/{game_id}"></a>
### 5.2 Get playoff result by year and specific game
- **Endpoint:** `/league_playoff_series_result_{year}/game/{game_id}/`
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
crashcrab.ddns.net/{YOUR_API_KEY}/league_playoff_series_result_20212022/game/202205040LAK/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_playoff_series_result_now/game/202205040LAK/
```
<a name="league_playoff_series_result_{year}/date/{game_date}"></a>
### 5.3 Get playoff result by year and specific date
- **Endpoint:** `/league_playoff_series_result_{year}/date/{game_date}/`
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
crashcrab.ddns.net/{YOUR_API_KEY}/league_playoff_series_result_2022/date/2022-05-04/
```
##### Example using for the current year
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_playoff_series_result_now/date/2022-05-04/
```
