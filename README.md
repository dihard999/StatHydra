# :crab:CrashCrab API
This application is a powerful API for sports analytics and match prediction, leveraging state-of-the-art machine learning algorithms. Designed for enthusiasts, analysts, and developers. With its robust and scalable architecture, the API offers seamless integration and real-time predictions, making it an essential tool for anyone seeking data-driven insights into the world of sports.  
---
---
# Table of Data
1. [Base URL](#base-url)
2. [Player](#player)
3. [Team](#team)  
   3.1 [Get all season teams statistics summary(except for the current season)](#team_all_season_summary)  
   3.2 [Get all season teams statistics summary by specific team(except for the current season)](#team_all_season_summary/{abbreviation}) 
4. [Season](#season)  
   4.1 [Get summary statistic by year](#season_summary_{year})  
   4.2 [Get summary statistic by year and specific team](#season_summary_{year}/{abbreviation})  
   4.3 [Get summary statistic for the current season](#season_summary_now)
6. [Game](#game)
---
## Base URL
All endpoints referenced in this section are relative to the following base URL:  
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/api/v1/
```
Your unique API Key required for accessing the API endpoints. Substitute YOUR_API_KEY with your actual key in the URL path.

---
## Player
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
  - **`games`** (integer) - Games Played (GP). Total number of games played by the team during the regular season (all season). (except current season).
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout (all season). (except current season).
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout (all season). (except current season).
  - **`losses_ot`** (integer) - Overtime/Shootout Losses (OL). Total number of games lost by the team in overtime or shootout for all season (relevant from 2000 season onward).
  - **`points`** (integer) - Points (PTS). Total points accumulated by the team during the regular season. (except current season).
  - **`points_pct`** (number, decimal) - Points (PTS). Total points accumulated by the team during the regular season. (except current season).
  - **`years_playoffs`** (integer) - Number of years team made the playoffs.
  - **`years_division_champion`** (integer) - Number of years team finished first (or tied for first) in the division.
  - **`years_conference_champion`** (integer) - Years team won the playoff conference championship. This begins in 1981-82.
  - **`years_league_champion`** (integer) - Years team won the league championship.
  - **`years_cup_champion`** (integer) - Years team won the Stanley Cup.

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/api/v1/team_all_season_summary/
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
  - **`games`** (integer) - Games Played (GP). Total number of games played by the team during the regular season (all season). (except current season).
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout (all season). (except current season).
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout (all season). (except current season).
  - **`losses_ot`** (integer) - Overtime/Shootout Losses (OL). Total number of games lost by the team in overtime or shootout for all season (relevant from 2000 season onward).
  - **`points`** (integer) - Points (PTS). Total points accumulated by the team during the regular season. (except current season).
  - **`points_pct`** (number, decimal) - Points (PTS). Total points accumulated by the team during the regular season. (except current season).
  - **`years_playoffs`** (integer) - Number of years team made the playoffs.
  - **`years_division_champion`** (integer) - Number of years team finished first (or tied for first) in the division.
  - **`years_conference_champion`** (integer) - Years team won the playoff conference championship. This begins in 1981-82.
  - **`years_league_champion`** (integer) - Years team won the league championship.
  - **`years_cup_champion`** (integer) - Years team won the Stanley Cup.

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/api/v1/team_all_season_summary/TOR
```
---
## Season  
<a name="season_summary_{year}"></a>
### Get summary statistic by year
- **Endpoint:** `/season_summary_{year}/`
- **Method:** GET
- **Description:** Get summary statistics for all teams for a specific season years
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "2012", "2018", "2024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`team_name`** (string) - Full team name. The name of the NHL team.
  - **`abbreviation`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`conference`** (string) - Conference the team played in during the season. May be null if not applicable.
  - **`division`** (string) - Division the team played in during the season. May be null if not applicable.
  - **`playoff`** (string) - Indicator if the team made the playoffs that season (e.g., 'Yes', 'No).
  - **`games`** (integer) - Games Played (GP). Total number of games played by the team during the regular season.
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout.
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout.
  - **`losses_ot`** (integer) - Overtime/Shootout Losses (OL). Total number of games lost by the team in overtime or shootout (relevant from 2000 season onward).
  - **`points`** (integer) - Points (PTS). Total points accumulated by the team during the regular season.
  - **`points_pct`** (number, decimal) - Points Percentage (PTS%). The percentage of total possible points earned by the team. Calculated as PTS / (GP * 2). Useful for comparing teams with different numbers of games played. Expressed as a decimal (e.g., 0.571).
  - **`goals`** (integer) - Goals For (GF). Total number of goals scored by the team during the season. Reflects the team's offensive performance.
  - **`goals_against`** (integer) - Goals Against (GL). Total number of goals conceded by the team during the season. Reflects the team's defensive performance.
  - **`srs`** (number, decimal) - Simple Rating System (SRS). A team rating that combines goal differential and strength of schedule. Higher values indicate stronger teams. Expressed as a decimal (e.g., 0.571).
  - **`sos`** (number, decimal) - Strength of Schedule (SOS). A measure of how difficult a team's schedule was during the season. Positive values mean tougher opponents; negative values mean weaker opponents. Zero represents an average team. Expressed as a decimal (e.g., 0.571).
  - **`reg_wins`** (integer) - Number of wins achieved in regulation or overtime (ROW).
  - **`points_pct_old`** (number, decimal) - Points percentage calculated without awarding any points for an overtime loss. Expressed as a decimal (e.g., 0.571).
  - **`reg_rec`** (string) - Regulation time record (W-L-T format likely) in regulation time only.
  - **`points_pct_reg`** (number, decimal) - Points percentage based only on regulation time results. Expressed as a decimal (e.g., 0.571).

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/api/v1/season_summary_2021/
```
<a name="season_summary_{year}/{abbreviation}"></a>
### Get summary statistic by year and specific team 
- **Endpoint:** `/season_summary_{year}/{abbreviation}`
- **Method:** GET
- **Description:** Get summary statistics for a specific team for a specific season year
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "2012", "2018", "2024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{abbreviation}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`team_name`** (string) - Full team name. The name of the NHL team.
  - **`abbreviation`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`conference`** (string) - Conference the team played in during the season. May be null if not applicable.
  - **`division`** (string) - Division the team played in during the season. May be null if not applicable.
  - **`playoff`** (string) - Indicator if the team made the playoffs that season (e.g., 'Yes', 'No).
  - **`games`** (integer) - Games Played (GP). Total number of games played by the team during the regular season.
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout.
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout.
  - **`losses_ot`** (integer) - Overtime/Shootout Losses (OL). Total number of games lost by the team in overtime or shootout (relevant from 2000 season onward).
  - **`points`** (integer) - Points (PTS). Total points accumulated by the team during the regular season.
  - **`points_pct`** (number, decimal) - Points Percentage (PTS%). The percentage of total possible points earned by the team. Calculated as PTS / (GP * 2). Useful for comparing teams with different numbers of games played. Expressed as a decimal (e.g., 0.571).
  - **`goals`** (integer) - Goals For (GF). Total number of goals scored by the team during the season. Reflects the team's offensive performance.
  - **`goals_against`** (integer) - Goals Against (GL). Total number of goals conceded by the team during the season. Reflects the team's defensive performance.
  - **`srs`** (number, decimal) - Simple Rating System (SRS). A team rating that combines goal differential and strength of schedule. Higher values indicate stronger teams. Expressed as a decimal (e.g., 0.571).
  - **`sos`** (number, decimal) - Strength of Schedule (SOS). A measure of how difficult a team's schedule was during the season. Positive values mean tougher opponents; negative values mean weaker opponents. Zero represents an average team. Expressed as a decimal (e.g., 0.571).
  - **`reg_wins`** (integer) - Number of wins achieved in regulation or overtime (ROW).
  - **`points_pct_old`** (number, decimal) - Points percentage calculated without awarding any points for an overtime loss. Expressed as a decimal (e.g., 0.571).
  - **`reg_rec`** (string) - Regulation time record (W-L-T format likely) in regulation time only.
  - **`points_pct_reg`** (number, decimal) - Points percentage based only on regulation time results. Expressed as a decimal (e.g., 0.571).

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/api/v1/season_summary_2021/TOR
```
<a name="season_summary_now"></a>
### Get summary statistic for the current season 
- **Endpoint:** `/season_summary_now/`
- **Method:** GET
- **Description:** Summary statistics of all teams for the current season
- **Parameters:** No
- **Response:** JSON format
- **Schema table:**
  - **`team_name`** (string) - Full team name. The name of the NHL team.
  - **`abbreviation`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`conference`** (string) - Conference the team played in during the season. May be null if not applicable.
  - **`division`** (string) - Division the team played in during the season. May be null if not applicable.
  - **`playoff`** (string) - Indicator if the team made the playoffs that season (e.g., 'Yes', 'No).
  - **`games`** (integer) - Games Played (GP). Total number of games played by the team during the regular season.
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout.
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout.
  - **`losses_ot`** (integer) - Overtime/Shootout Losses (OL). Total number of games lost by the team in overtime or shootout (relevant from 2000 season onward).
  - **`points`** (integer) - Points (PTS). Total points accumulated by the team during the regular season.
  - **`points_pct`** (number, decimal) - Points Percentage (PTS%). The percentage of total possible points earned by the team. Calculated as PTS / (GP * 2). Useful for comparing teams with different numbers of games played. Expressed as a decimal (e.g., 0.571).
  - **`goals`** (integer) - Goals For (GF). Total number of goals scored by the team during the season. Reflects the team's offensive performance.
  - **`goals_against`** (integer) - Goals Against (GL). Total number of goals conceded by the team during the season. Reflects the team's defensive performance.
  - **`srs`** (number, decimal) - Simple Rating System (SRS). A team rating that combines goal differential and strength of schedule. Higher values indicate stronger teams. Expressed as a decimal (e.g., 0.571).
  - **`sos`** (number, decimal) - Strength of Schedule (SOS). A measure of how difficult a team's schedule was during the season. Positive values mean tougher opponents; negative values mean weaker opponents. Zero represents an average team. Expressed as a decimal (e.g., 0.571).
  - **`reg_wins`** (integer) - Number of wins achieved in regulation or overtime (ROW).
  - **`points_pct_old`** (number, decimal) - Points percentage calculated without awarding any points for an overtime loss. Expressed as a decimal (e.g., 0.571).
  - **`reg_rec`** (string) - Regulation time record (W-L-T format likely) in regulation time only.
  - **`points_pct_reg`** (number, decimal) - Points percentage based only on regulation time results. Expressed as a decimal (e.g., 0.571).

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/api/v1/season_summary_now/
```

---
## Game
