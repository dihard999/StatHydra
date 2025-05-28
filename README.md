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
   4.1 [Get summary statistic season by year](#season_summary_{year})  
   4.2 [Get summary statistic season by year and specific team](#season_summary_{year}/{abbreviation})  
   4.3 [Get summary statistic for the current season](#season_summary_now)  
   4.4 [Get summary statistic for the current season and specific team](#season_summary_now/{abbreviation})  
   4.5 [Get detail statistic season by year](#season_statistics_{year})  
   4.6 [Get detail statistic season by year and specific team](#season_statistics_{year}/{abbreviation})  
   4.7 [Get detail statistic season for the current season](#season_statistics_now)  
   4.8 [Get detail statistic season for the current season and specific team](#season_statistics_now/{abbreviation})  
   4.9 [Get league average by year](#league_average_{year})  
   4.10 [Get league average for the current season](#league_average_now)
6. [Game](#game)
---
<a name="base-url"></a>
## 1. Base URL
All endpoints referenced in this section are relative to the following base URL:  
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/api/v1/
```
Your unique API Key required for accessing the API endpoints. Substitute YOUR_API_KEY with your actual key in the URL path.

---
<a name="player"></a>
## 2. Player
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
<a name="season"></a>
## 4. Season  
<a name="season_summary_{year}"></a>
### 4.1 Get summary statistic season by year
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
### 4.2 Get summary statistic season by year and specific team 
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
### 4.3 Get summary statistic for the current season 
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
<a name="season_summary_now/{abbreviation}"></a>
### 4.4 Get summary statistic for the current season and specific team
- **Endpoint:** `/season_summary_now/{abbreviation}/`
- **Method:** GET
- **Description:** Summary statistics of a specific team for current season
- **Parameters:**
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
crashcrab.ddns.net/{YOUR_API_KEY}/api/v1/season_summary_now/TOR/
```
<a name="season_statistics_{year}"></a>
### 4.5 Get detail statistic season by year
- **Endpoint:** `/season_statistics_{year}/`
- **Method:** GET
- **Description:** Detail statistics of all teams for the specific season
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "2012", "2018", "2024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`ranker`** (integer) - Rank. The ranking of the team in the league based on their performance. A lower number (e.g., 1) indicates a higher-ranked team.
  - **`team_name`** (string) - Full team name. The name of the NHL team.
  - **`abbreviation`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`average_age`** (number, decimal) - Average Age (AvAge). Average age of team weighted by time on ice. Expressed as a decimal (e.g., 0.571).
  - **`playoff`** (string) - Indicator if the team made the playoffs that season (e.g., 'Yes', 'No).
  - **`games`** (integer) - Games Played (GP). Total number of games played by the team during the regular season.
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout.
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout.
  - **`losses_ot`** (integer) - Overtime/Shootout Losses (OL). Total number of games lost by the team in overtime or shootout (relevant from 2000 season onward).
  - **`points`** (integer) - Points (PTS). Total points accumulated by the team during the regular season.
  - **`points_pct`** (number, decimal) - Points Percentage (PTS%). The percentage of total possible points earned by the team. Calculated as PTS / (GP * 2). Useful for comparing teams with different numbers of games played. Expressed as a decimal (e.g., 0.571).
  - **`goals`** (integer) - Goals For (GF). Total number of goals scored by the team during the season. Reflects the team's offensive performance.
  - **`goals_against`** (integer) - Goals Against (GL). Total number of goals conceded by the team during the season. Reflects the team's defensive performance.
  - **`wins_shootout`** (integer) - Shootout Wins (SOW). Total number of games won by the team in shootouts. Shootout wins are a subset of overall wins.
  - **`losses_shootout`** (integer) - Shootout Losses (SOL). Total number of games lost by the team in shootouts.
  - **`srs`** (number, decimal) - Simple Rating System (SRS). A team rating that combines goal differential and strength of schedule. Higher values indicate stronger teams. Expressed as a decimal (e.g., 0.571).
  - **`sos`** (number, decimal) - Strength of Schedule (SOS). A measure of how difficult a team's schedule was during the season. Positive values mean tougher opponents; negative values mean weaker opponents. Zero represents an average team. Expressed as a decimal (e.g., 0.571).
  - **`goals_for_per_game`** (number, decimal) - Goals For Per Game (GF/G). Average number of goals scored by the team per game. Reflects offensive efficiency. Expressed as a decimal (e.g., 3.12).
  - **`goals_against_per_game`** (number, decimal) - Goals Against Per Game (GA/G). Average number of goals conceded by the team per game. Reflects defensive efficiency. Expressed as a decimal (e.g., 2.57).
  - **`goals_pp`** (integer) - Power Play Goals (PP). Total number of goals scored by the team during power play situations. Indicates power play effectiveness.
  - **`chances_pp`** (integer) - Power Play Opportunities (PPO). Total number of power play opportunities the team had during the season. Reflects chances to use man advantage.
  - **`power_play_pct`** (number, decimal) - Power Play Percentage (PP%). Percentage of power play opportunities converted into goals. Calculated as (PP / PPO) * 100. Higher values indicate better power play performance. Expressed as a decimal (e.g., 0.221).
  - **`opp_goals_pp`** (integer) - Power Play Goals Against (PPA). Total number of goals conceded by the team during opposing power plays. Reflects penalty-killing effectiveness.
  - **`opp_chances_pp`** (integer) - Power Play Opportunities Against (PPOA). Total number of power play opportunities the opposing team had against them. Indicates how often the team had to kill penalties.
  - **`pen_kill_pct`** (number, decimal) - Penalty Kill Percentage (PK%). Percentage of opposing power play opportunities successfully killed off. Higher percentages indicate better penalty-killing performance. Expressed as a decimal (e.g., 0.837).
  - **`goals_sh`** (integer) - Short-Handed Goals (SH). Total number of short-handed goals scored by the team. Goals scored while the team was on the penalty kill.
  - **`opp_goals_sh`** (integer) - Short-Handed Goals Against (SHA). Total number of short-handed goals conceded by the team. Goals scored by the opposing team while on the penalty kill.
  - **`pen_min_per_game`** (number, decimal) - Penalties in Minutes Per Game (PIM/G). Average number of penalty minutes per game for the team. Reflects the team's discipline or lack thereof. Expressed as a decimal (e.g., 0.571).
  - **`pen_min_per_game_opp`** (number, decimal) - Opponent Penalties in Minutes Per Game (oPIM/G). Average number of penalty minutes per game for the opposing team. Shows how often rivals are penalized (e.g., 9.3)
  - **`shots`** (integer) - Shots on Goal (S). Total number of shots on goal taken by the team during the season. Reflects offensive activity.
  - **`shot_pct`** (number, decimal) - Shooting Percentage (S%). Percentage of shots on goal that resulted in goals. Calculated as (GF / S) * 100. Expressed as a decimal (e.g., 0.095).
  - **`shots_against`** (integer) - Shots Against (SA). Total number of shots on goal taken by opponents against the team. Reflects defensive pressure faced.
  - **`save_pct`** (number, decimal) - Save Percentage (SV%). Percentage of shots on goal stopped by the team's goaltenders. Calculated as 1 - (GA / SA). Higher values mean better goaltending. Expressed as a decimal (e.g., 0.911).
  - **`shutouts`** (integer) - Shutouts (SO). Total number of games in which the team did not allow any goals. Reflects strong defensive and goaltending performances.

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/api/v1/season_statistics_2022/
```

<a name="season_statistics_{year}/{abbreviation}"></a>
### 4.6 Get detail statistic season by year and specific team
- **Endpoint:** `/season_statistics_{year}/{abbreviation}/`
- **Method:** GET
- **Description:** Detail statistics of a specific team for specific season
- **Parameters:**
   - **`{year}`** (integer) - A dynamic prefix identifying a season or data set (e.g. "2012", "2018", "2024"). This prefix is ​​part of the path and is used to identify the data table.
   - **`{abbreviation}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`ranker`** (integer) - Rank. The ranking of the team in the league based on their performance. A lower number (e.g., 1) indicates a higher-ranked team.
  - **`team_name`** (string) - Full team name. The name of the NHL team.
  - **`abbreviation`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`average_age`** (number, decimal) - Average Age (AvAge). Average age of team weighted by time on ice. Expressed as a decimal (e.g., 0.571).
  - **`playoff`** (string) - Indicator if the team made the playoffs that season (e.g., 'Yes', 'No).
  - **`games`** (integer) - Games Played (GP). Total number of games played by the team during the regular season.
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout.
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout.
  - **`losses_ot`** (integer) - Overtime/Shootout Losses (OL). Total number of games lost by the team in overtime or shootout (relevant from 2000 season onward).
  - **`points`** (integer) - Points (PTS). Total points accumulated by the team during the regular season.
  - **`points_pct`** (number, decimal) - Points Percentage (PTS%). The percentage of total possible points earned by the team. Calculated as PTS / (GP * 2). Useful for comparing teams with different numbers of games played. Expressed as a decimal (e.g., 0.571).
  - **`goals`** (integer) - Goals For (GF). Total number of goals scored by the team during the season. Reflects the team's offensive performance.
  - **`goals_against`** (integer) - Goals Against (GL). Total number of goals conceded by the team during the season. Reflects the team's defensive performance.
  - **`wins_shootout`** (integer) - Shootout Wins (SOW). Total number of games won by the team in shootouts. Shootout wins are a subset of overall wins.
  - **`losses_shootout`** (integer) - Shootout Losses (SOL). Total number of games lost by the team in shootouts.
  - **`srs`** (number, decimal) - Simple Rating System (SRS). A team rating that combines goal differential and strength of schedule. Higher values indicate stronger teams. Expressed as a decimal (e.g., 0.571).
  - **`sos`** (number, decimal) - Strength of Schedule (SOS). A measure of how difficult a team's schedule was during the season. Positive values mean tougher opponents; negative values mean weaker opponents. Zero represents an average team. Expressed as a decimal (e.g., 0.571).
  - **`goals_for_per_game`** (number, decimal) - Goals For Per Game (GF/G). Average number of goals scored by the team per game. Reflects offensive efficiency. Expressed as a decimal (e.g., 3.12).
  - **`goals_against_per_game`** (number, decimal) - Goals Against Per Game (GA/G). Average number of goals conceded by the team per game. Reflects defensive efficiency. Expressed as a decimal (e.g., 2.57).
  - **`goals_pp`** (integer) - Power Play Goals (PP). Total number of goals scored by the team during power play situations. Indicates power play effectiveness.
  - **`chances_pp`** (integer) - Power Play Opportunities (PPO). Total number of power play opportunities the team had during the season. Reflects chances to use man advantage.
  - **`power_play_pct`** (number, decimal) - Power Play Percentage (PP%). Percentage of power play opportunities converted into goals. Calculated as (PP / PPO) * 100. Higher values indicate better power play performance. Expressed as a decimal (e.g., 0.221).
  - **`opp_goals_pp`** (integer) - Power Play Goals Against (PPA). Total number of goals conceded by the team during opposing power plays. Reflects penalty-killing effectiveness.
  - **`opp_chances_pp`** (integer) - Power Play Opportunities Against (PPOA). Total number of power play opportunities the opposing team had against them. Indicates how often the team had to kill penalties.
  - **`pen_kill_pct`** (number, decimal) - Penalty Kill Percentage (PK%). Percentage of opposing power play opportunities successfully killed off. Higher percentages indicate better penalty-killing performance. Expressed as a decimal (e.g., 0.837).
  - **`goals_sh`** (integer) - Short-Handed Goals (SH). Total number of short-handed goals scored by the team. Goals scored while the team was on the penalty kill.
  - **`opp_goals_sh`** (integer) - Short-Handed Goals Against (SHA). Total number of short-handed goals conceded by the team. Goals scored by the opposing team while on the penalty kill.
  - **`pen_min_per_game`** (number, decimal) - Penalties in Minutes Per Game (PIM/G). Average number of penalty minutes per game for the team. Reflects the team's discipline or lack thereof. Expressed as a decimal (e.g., 0.571).
  - **`pen_min_per_game_opp`** (number, decimal) - Opponent Penalties in Minutes Per Game (oPIM/G). Average number of penalty minutes per game for the opposing team. Shows how often rivals are penalized (e.g., 9.3)
  - **`shots`** (integer) - Shots on Goal (S). Total number of shots on goal taken by the team during the season. Reflects offensive activity.
  - **`shot_pct`** (number, decimal) - Shooting Percentage (S%). Percentage of shots on goal that resulted in goals. Calculated as (GF / S) * 100. Expressed as a decimal (e.g., 0.095).
  - **`shots_against`** (integer) - Shots Against (SA). Total number of shots on goal taken by opponents against the team. Reflects defensive pressure faced.
  - **`save_pct`** (number, decimal) - Save Percentage (SV%). Percentage of shots on goal stopped by the team's goaltenders. Calculated as 1 - (GA / SA). Higher values mean better goaltending. Expressed as a decimal (e.g., 0.911).
  - **`shutouts`** (integer) - Shutouts (SO). Total number of games in which the team did not allow any goals. Reflects strong defensive and goaltending performances.

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/api/v1/season_statistics_2022/TOR/
```
<a name="season_statistics_now"></a>
### 4.7 Get detail statistic season for the current season
- **Endpoint:** `/season_statistics_now/`
- **Method:** GET
- **Description:** Statistics of all teams for the current season
- **Parameters:** No
- **Response:** JSON format
- **Schema table:**
  - **`ranker`** (integer) - Rank. The ranking of the team in the league based on their performance. A lower number (e.g., 1) indicates a higher-ranked team.
  - **`team_name`** (string) - Full team name. The name of the NHL team.
  - **`abbreviation`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`average_age`** (number, decimal) - Average Age (AvAge). Average age of team weighted by time on ice. Expressed as a decimal (e.g., 0.571).
  - **`playoff`** (string) - Indicator if the team made the playoffs that season (e.g., 'Yes', 'No).
  - **`games`** (integer) - Games Played (GP). Total number of games played by the team during the regular season.
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout.
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout.
  - **`losses_ot`** (integer) - Overtime/Shootout Losses (OL). Total number of games lost by the team in overtime or shootout (relevant from 2000 season onward).
  - **`points`** (integer) - Points (PTS). Total points accumulated by the team during the regular season.
  - **`points_pct`** (number, decimal) - Points Percentage (PTS%). The percentage of total possible points earned by the team. Calculated as PTS / (GP * 2). Useful for comparing teams with different numbers of games played. Expressed as a decimal (e.g., 0.571).
  - **`goals`** (integer) - Goals For (GF). Total number of goals scored by the team during the season. Reflects the team's offensive performance.
  - **`goals_against`** (integer) - Goals Against (GL). Total number of goals conceded by the team during the season. Reflects the team's defensive performance.
  - **`wins_shootout`** (integer) - Shootout Wins (SOW). Total number of games won by the team in shootouts. Shootout wins are a subset of overall wins.
  - **`losses_shootout`** (integer) - Shootout Losses (SOL). Total number of games lost by the team in shootouts.
  - **`srs`** (number, decimal) - Simple Rating System (SRS). A team rating that combines goal differential and strength of schedule. Higher values indicate stronger teams. Expressed as a decimal (e.g., 0.571).
  - **`sos`** (number, decimal) - Strength of Schedule (SOS). A measure of how difficult a team's schedule was during the season. Positive values mean tougher opponents; negative values mean weaker opponents. Zero represents an average team. Expressed as a decimal (e.g., 0.571).
  - **`goals_for_per_game`** (number, decimal) - Goals For Per Game (GF/G). Average number of goals scored by the team per game. Reflects offensive efficiency. Expressed as a decimal (e.g., 3.12).
  - **`goals_against_per_game`** (number, decimal) - Goals Against Per Game (GA/G). Average number of goals conceded by the team per game. Reflects defensive efficiency. Expressed as a decimal (e.g., 2.57).
  - **`goals_pp`** (integer) - Power Play Goals (PP). Total number of goals scored by the team during power play situations. Indicates power play effectiveness.
  - **`chances_pp`** (integer) - Power Play Opportunities (PPO). Total number of power play opportunities the team had during the season. Reflects chances to use man advantage.
  - **`power_play_pct`** (number, decimal) - Power Play Percentage (PP%). Percentage of power play opportunities converted into goals. Calculated as (PP / PPO) * 100. Higher values indicate better power play performance. Expressed as a decimal (e.g., 0.221).
  - **`opp_goals_pp`** (integer) - Power Play Goals Against (PPA). Total number of goals conceded by the team during opposing power plays. Reflects penalty-killing effectiveness.
  - **`opp_chances_pp`** (integer) - Power Play Opportunities Against (PPOA). Total number of power play opportunities the opposing team had against them. Indicates how often the team had to kill penalties.
  - **`pen_kill_pct`** (number, decimal) - Penalty Kill Percentage (PK%). Percentage of opposing power play opportunities successfully killed off. Higher percentages indicate better penalty-killing performance. Expressed as a decimal (e.g., 0.837).
  - **`goals_sh`** (integer) - Short-Handed Goals (SH). Total number of short-handed goals scored by the team. Goals scored while the team was on the penalty kill.
  - **`opp_goals_sh`** (integer) - Short-Handed Goals Against (SHA). Total number of short-handed goals conceded by the team. Goals scored by the opposing team while on the penalty kill.
  - **`pen_min_per_game`** (number, decimal) - Penalties in Minutes Per Game (PIM/G). Average number of penalty minutes per game for the team. Reflects the team's discipline or lack thereof. Expressed as a decimal (e.g., 0.571).
  - **`pen_min_per_game_opp`** (number, decimal) - Opponent Penalties in Minutes Per Game (oPIM/G). Average number of penalty minutes per game for the opposing team. Shows how often rivals are penalized (e.g., 9.3)
  - **`shots`** (integer) - Shots on Goal (S). Total number of shots on goal taken by the team during the season. Reflects offensive activity.
  - **`shot_pct`** (number, decimal) - Shooting Percentage (S%). Percentage of shots on goal that resulted in goals. Calculated as (GF / S) * 100. Expressed as a decimal (e.g., 0.095).
  - **`shots_against`** (integer) - Shots Against (SA). Total number of shots on goal taken by opponents against the team. Reflects defensive pressure faced.
  - **`save_pct`** (number, decimal) - Save Percentage (SV%). Percentage of shots on goal stopped by the team's goaltenders. Calculated as 1 - (GA / SA). Higher values mean better goaltending. Expressed as a decimal (e.g., 0.911).
  - **`shutouts`** (integer) - Shutouts (SO). Total number of games in which the team did not allow any goals. Reflects strong defensive and goaltending performances.

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/api/v1/season_statistics_now/
```

<a name="season_statistics_now/{abbreviation}"></a>
### 4.8 Get detail statistic season for the current season and specific team
- **Endpoint:** `/season_statistics_now/{abbreviation}/`
- **Method:** GET
- **Description:** Detail statistics of a specific team for current season
- **Parameters:**
   - **`{abbreviation}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`ranker`** (integer) - Rank. The ranking of the team in the league based on their performance. A lower number (e.g., 1) indicates a higher-ranked team.
  - **`team_name`** (string) - Full team name. The name of the NHL team.
  - **`abbreviation`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`average_age`** (number, decimal) - Average Age (AvAge). Average age of team weighted by time on ice. Expressed as a decimal (e.g., 0.571).
  - **`playoff`** (string) - Indicator if the team made the playoffs that season (e.g., 'Yes', 'No).
  - **`games`** (integer) - Games Played (GP). Total number of games played by the team during the regular season.
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout.
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout.
  - **`losses_ot`** (integer) - Overtime/Shootout Losses (OL). Total number of games lost by the team in overtime or shootout (relevant from 2000 season onward).
  - **`points`** (integer) - Points (PTS). Total points accumulated by the team during the regular season.
  - **`points_pct`** (number, decimal) - Points Percentage (PTS%). The percentage of total possible points earned by the team. Calculated as PTS / (GP * 2). Useful for comparing teams with different numbers of games played. Expressed as a decimal (e.g., 0.571).
  - **`goals`** (integer) - Goals For (GF). Total number of goals scored by the team during the season. Reflects the team's offensive performance.
  - **`goals_against`** (integer) - Goals Against (GL). Total number of goals conceded by the team during the season. Reflects the team's defensive performance.
  - **`wins_shootout`** (integer) - Shootout Wins (SOW). Total number of games won by the team in shootouts. Shootout wins are a subset of overall wins.
  - **`losses_shootout`** (integer) - Shootout Losses (SOL). Total number of games lost by the team in shootouts.
  - **`srs`** (number, decimal) - Simple Rating System (SRS). A team rating that combines goal differential and strength of schedule. Higher values indicate stronger teams. Expressed as a decimal (e.g., 0.571).
  - **`sos`** (number, decimal) - Strength of Schedule (SOS). A measure of how difficult a team's schedule was during the season. Positive values mean tougher opponents; negative values mean weaker opponents. Zero represents an average team. Expressed as a decimal (e.g., 0.571).
  - **`goals_for_per_game`** (number, decimal) - Goals For Per Game (GF/G). Average number of goals scored by the team per game. Reflects offensive efficiency. Expressed as a decimal (e.g., 3.12).
  - **`goals_against_per_game`** (number, decimal) - Goals Against Per Game (GA/G). Average number of goals conceded by the team per game. Reflects defensive efficiency. Expressed as a decimal (e.g., 2.57).
  - **`goals_pp`** (integer) - Power Play Goals (PP). Total number of goals scored by the team during power play situations. Indicates power play effectiveness.
  - **`chances_pp`** (integer) - Power Play Opportunities (PPO). Total number of power play opportunities the team had during the season. Reflects chances to use man advantage.
  - **`power_play_pct`** (number, decimal) - Power Play Percentage (PP%). Percentage of power play opportunities converted into goals. Calculated as (PP / PPO) * 100. Higher values indicate better power play performance. Expressed as a decimal (e.g., 0.221).
  - **`opp_goals_pp`** (integer) - Power Play Goals Against (PPA). Total number of goals conceded by the team during opposing power plays. Reflects penalty-killing effectiveness.
  - **`opp_chances_pp`** (integer) - Power Play Opportunities Against (PPOA). Total number of power play opportunities the opposing team had against them. Indicates how often the team had to kill penalties.
  - **`pen_kill_pct`** (number, decimal) - Penalty Kill Percentage (PK%). Percentage of opposing power play opportunities successfully killed off. Higher percentages indicate better penalty-killing performance. Expressed as a decimal (e.g., 0.837).
  - **`goals_sh`** (integer) - Short-Handed Goals (SH). Total number of short-handed goals scored by the team. Goals scored while the team was on the penalty kill.
  - **`opp_goals_sh`** (integer) - Short-Handed Goals Against (SHA). Total number of short-handed goals conceded by the team. Goals scored by the opposing team while on the penalty kill.
  - **`pen_min_per_game`** (number, decimal) - Penalties in Minutes Per Game (PIM/G). Average number of penalty minutes per game for the team. Reflects the team's discipline or lack thereof. Expressed as a decimal (e.g., 0.571).
  - **`pen_min_per_game_opp`** (number, decimal) - Opponent Penalties in Minutes Per Game (oPIM/G). Average number of penalty minutes per game for the opposing team. Shows how often rivals are penalized (e.g., 9.3)
  - **`shots`** (integer) - Shots on Goal (S). Total number of shots on goal taken by the team during the season. Reflects offensive activity.
  - **`shot_pct`** (number, decimal) - Shooting Percentage (S%). Percentage of shots on goal that resulted in goals. Calculated as (GF / S) * 100. Expressed as a decimal (e.g., 0.095).
  - **`shots_against`** (integer) - Shots Against (SA). Total number of shots on goal taken by opponents against the team. Reflects defensive pressure faced.
  - **`save_pct`** (number, decimal) - Save Percentage (SV%). Percentage of shots on goal stopped by the team's goaltenders. Calculated as 1 - (GA / SA). Higher values mean better goaltending. Expressed as a decimal (e.g., 0.911).
  - **`shutouts`** (integer) - Shutouts (SO). Total number of games in which the team did not allow any goals. Reflects strong defensive and goaltending performances.

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/api/v1/season_statistics_now/{abbreviation}/
```
<a name="league_average_{year}"></a>
### 4.9 Get league average by year
- **Endpoint:** `/league_average_{year}/`
- **Method:** GET
- **Description:** League average for the specific season
- **Parameters:**
   - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "2012", "2018", "2024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - average_age (number, decimal) - Average Age (AvAge). Average age of team weighted by time on ice. Expressed as a decimal (e.g., 27.4).
  - games (integer) - Games Played (GP). Total number of games played by the team during the regular season.
  - wins (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout.
  - losses (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout.
  - losses_ot (integer) - Overtime/Shootout Losses (OL). Total number of games lost by the team in overtime or shootout (relevant from 2000 season onward).
  - points (integer) - Points (PTS). Total points accumulated by the team during the regular season. Teams earn 2 points for a win, 1 point for an overtime/shootout loss, and 0 points for a regulation loss.
  - points_pct (number, decimal) - Points Percentage (PTS%). The percentage of total possible points earned by the team. Calculated as PTS / (GP * 2). Useful for comparing teams with different numbers of games played. Expressed as a decimal (e.g., 0.671).
  - **`goals`** (integer) - Goals For (GF). Total number of goals scored by the team during the season. Reflects the team's offensive performance.
  - **`goals_against`** (integer) - Goals Against (GL). Total number of goals conceded by the team during the season. Reflects the team's defensive performance.
  - **`goals_pp`** (integer) - Power Play Goals (PP). Total number of goals scored by the team during power play situations. Indicates power play effectiveness.
  - **`chances_pp`** (integer) - Power Play Opportunities (PPO). Total number of power play opportunities the team had during the season. Reflects chances to use man advantage.
  - **`power_play_pct`** (number, decimal) - Power Play Percentage (PP%). Percentage of power play opportunities converted into goals. Calculated as (PP / PPO) * 100. Higher values indicate better power play performance. Expressed as a decimal (e.g., 0.221).
  - **`opp_goals_pp`** (integer) - Power Play Goals Against (PPA). Total number of goals conceded by the team during opposing power plays. Reflects penalty-killing effectiveness.
  - **`opp_chances_pp`** (integer) - Power Play Opportunities Against (PPOA). Total number of power play opportunities the opposing team had against them. Indicates how often the team had to kill penalties.
  - **`pen_kill_pct`** (number, decimal) - Penalty Kill Percentage (PK%). Percentage of opposing power play opportunities successfully killed off. Higher percentages indicate better penalty-killing performance. Expressed as a decimal (e.g., 0.837).
  - **`goals_sh`** (integer) - Short-Handed Goals (SH). Total number of short-handed goals scored by the team. Goals scored while the team was on the penalty kill.
  - **`opp_goals_sh`** (integer) - Short-Handed Goals Against (SHA). Total number of short-handed goals conceded by the team. Goals scored by the opposing team while on the penalty kill.
  - **`pen_min_per_game`** (number, decimal) - Penalties in Minutes Per Game (PIM/G). Average number of penalty minutes per game for the team. Reflects the team's discipline or lack thereof. Expressed as a decimal (e.g., 0.571).
  - **`pen_min_per_game_opp`** (number, decimal) - Opponent Penalties in Minutes Per Game (oPIM/G). Average number of penalty minutes per game for the opposing team. Shows how often rivals are penalized (e.g., 9.3)
  - **`shots`** (integer) - Shots on Goal (S). Total number of shots on goal taken by the team during the season. Reflects offensive activity.
  - **`shot_pct`** (number, decimal) - Shooting Percentage (S%). Percentage of shots on goal that resulted in goals. Calculated as (GF / S) * 100. Expressed as a decimal (e.g., 0.095).
  - **`shots_against`** (integer) - Shots Against (SA). Total number of shots on goal taken by opponents against the team. Reflects defensive pressure faced.
  - **`save_pct`** (number, decimal) - Save Percentage (SV%). Percentage of shots on goal stopped by the team's goaltenders. Calculated as 1 - (GA / SA). Higher values mean better goaltending. Expressed as a decimal (e.g., 0.911).
  - **`shutouts`** (integer) - Shutouts (SO). Total number of games in which the team did not allow any goals. Reflects strong defensive and goaltending performances.

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/api/v1/league_average_{year}/
```
<a name="league_average_now"></a>
### 4.10 Get league average for the current season
- **Endpoint:** `/league_average_now/`
- **Method:** GET
- **Description:** League average for the current season
- **Parameters:** No
- **Response:** JSON format
- **Schema table:**
  - average_age (number, decimal) - Average Age (AvAge). Average age of team weighted by time on ice. Expressed as a decimal (e.g., 27.4).
  - games (integer) - Games Played (GP). Total number of games played by the team during the regular season.
  - wins (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout.
  - losses (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout.
  - losses_ot (integer) - Overtime/Shootout Losses (OL). Total number of games lost by the team in overtime or shootout (relevant from 2000 season onward).
  - points (integer) - Points (PTS). Total points accumulated by the team during the regular season. Teams earn 2 points for a win, 1 point for an overtime/shootout loss, and 0 points for a regulation loss.
  - points_pct (number, decimal) - Points Percentage (PTS%). The percentage of total possible points earned by the team. Calculated as PTS / (GP * 2). Useful for comparing teams with different numbers of games played. Expressed as a decimal (e.g., 0.671).
  - **`goals`** (integer) - Goals For (GF). Total number of goals scored by the team during the season. Reflects the team's offensive performance.
  - **`goals_against`** (integer) - Goals Against (GL). Total number of goals conceded by the team during the season. Reflects the team's defensive performance.
  - **`goals_pp`** (integer) - Power Play Goals (PP). Total number of goals scored by the team during power play situations. Indicates power play effectiveness.
  - **`chances_pp`** (integer) - Power Play Opportunities (PPO). Total number of power play opportunities the team had during the season. Reflects chances to use man advantage.
  - **`power_play_pct`** (number, decimal) - Power Play Percentage (PP%). Percentage of power play opportunities converted into goals. Calculated as (PP / PPO) * 100. Higher values indicate better power play performance. Expressed as a decimal (e.g., 0.221).
  - **`opp_goals_pp`** (integer) - Power Play Goals Against (PPA). Total number of goals conceded by the team during opposing power plays. Reflects penalty-killing effectiveness.
  - **`opp_chances_pp`** (integer) - Power Play Opportunities Against (PPOA). Total number of power play opportunities the opposing team had against them. Indicates how often the team had to kill penalties.
  - **`pen_kill_pct`** (number, decimal) - Penalty Kill Percentage (PK%). Percentage of opposing power play opportunities successfully killed off. Higher percentages indicate better penalty-killing performance. Expressed as a decimal (e.g., 0.837).
  - **`goals_sh`** (integer) - Short-Handed Goals (SH). Total number of short-handed goals scored by the team. Goals scored while the team was on the penalty kill.
  - **`opp_goals_sh`** (integer) - Short-Handed Goals Against (SHA). Total number of short-handed goals conceded by the team. Goals scored by the opposing team while on the penalty kill.
  - **`pen_min_per_game`** (number, decimal) - Penalties in Minutes Per Game (PIM/G). Average number of penalty minutes per game for the team. Reflects the team's discipline or lack thereof. Expressed as a decimal (e.g., 0.571).
  - **`pen_min_per_game_opp`** (number, decimal) - Opponent Penalties in Minutes Per Game (oPIM/G). Average number of penalty minutes per game for the opposing team. Shows how often rivals are penalized (e.g., 9.3)
  - **`shots`** (integer) - Shots on Goal (S). Total number of shots on goal taken by the team during the season. Reflects offensive activity.
  - **`shot_pct`** (number, decimal) - Shooting Percentage (S%). Percentage of shots on goal that resulted in goals. Calculated as (GF / S) * 100. Expressed as a decimal (e.g., 0.095).
  - **`shots_against`** (integer) - Shots Against (SA). Total number of shots on goal taken by opponents against the team. Reflects defensive pressure faced.
  - **`save_pct`** (number, decimal) - Save Percentage (SV%). Percentage of shots on goal stopped by the team's goaltenders. Calculated as 1 - (GA / SA). Higher values mean better goaltending. Expressed as a decimal (e.g., 0.911).
  - **`shutouts`** (integer) - Shutouts (SO). Total number of games in which the team did not allow any goals. Reflects strong defensive and goaltending performances.

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/api/v1/league_average_now/
```

---
<a name="game"></a>
## 5. Game
