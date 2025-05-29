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
3. [Team](#team)  
   3.1 [Get all season teams statistics summary(except for the current season)](#team_all_season_summary)  
   3.2 [Get all season teams statistics summary by specific team(except for the current season)](#team_all_season_summary/{abbreviation})  
   3.3 [Get teams analytics 5 on 5 by year](#team_analytics_5_on_5_{year})  
   3.4 [Get teams analytics 5 on 5 by year and specific team](#team_analytics_5_on_5_{year}/{abbreviation})  
   3.5 [Get teams analytics 5 on 5 for the current season](#team_analytics_5_on_5_now)  
   3.6 [Get teams analytics 5 on 5 for the current season and specific team](#team_analytics_5_on_5_now/{abbreviation})
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
5. [Playoff](#playoff)  
   5.1 [Get playoff result by year](#league_playoff_series_result_{year})  
   5.2 [Get playoff result by year and specific game](#league_playoff_series_result_{year}/{game_id})  
   5.3 [Get playoff result by year and specific date](#league_playoff_series_result_{year}/date/{game_date})  
   5.4 [Get playoff result for the current season](#league_playoff_series_result_now)  
   5.5 [Get playoff result for the current season and specific game](#league_playoff_series_result_now/{game_id})  
   5.6 [Get playoff result for the current season and specific date](#league_playoff_series_result_now/date/{game_date})
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
  - **`shot_pct_5on5`** (number, decimal) - Shooting Percentage (S%) (5-on-5). Percentage of shots on goal that were scored at 5-on-5. Reflects shooting efficiency. Expressed as a decimal (e.g., 0.087).
  - **`shot_pct_5on5`** (number, decimal) - Shooting Percentage (S%) (5-on-5). Percentage of shots on goal that were scored at 5-on-5. Reflects shooting efficiency. Expressed as a decimal (e.g., 0.087).
  - **`pdo`** (number, decimal) - Shooting % + Save % (PDO). Sum of Shooting Percentage and Save Percentage at 5-on-5. Used as an indicator of puck luck. Expressed as a decimal (e.g., 1.008).
  - **`corsi_for_5on5`** (integer) - Corsi For (CF) (5-on-5). Measures the total number of shot attempts (including shots on goal, missed shots, and blocked shots) generated by a team while playing at even strength (5-on-5). Measures offensive possession.
  - **`corsi_against_5on5`** (integer) - Corsi Against (CA) (5-on-5). Measures the total number of shot attempts (including shots on goal, missed shots, and blocked shots) directed at the team's own net while playing at even strength (5-on-5). Measures defensive pressure faced.
  - **`corsi_pct_5on5`** (number, decimal) - Corsi For Percentage (CF%) (5-on-5). Percentage of total shot attempts controlled by the team at 5-on-5. Above 50% indicates puck control dominance. Expressed as a decimal (e.g., 0.527).
  - **`fenwick_for_5on5`** (integer) - Fenwick For (FF) (5-on-5). Total number of unblocked shot attempts (shots + misses) by the team at 5-on-5. Like Corsi, but excludes blocked shots.
  - **`fenwick_against_5on5`** (integer) - Fenwick Against (FA) (5-on-5). Total number of unblocked shot attempts (shots + misses) allowed by the team at 5-on-5. Like Corsi, but excludes blocked shots.
  - **`fenwick_against_5on5`** (integer) - Fenwick Against (FA) (5-on-5). Total number of unblocked shot attempts (shots + misses) allowed by the team at 5-on-5. Like Corsi, but excludes blocked shots.
  - **`opp_chances_pp`** (integer) - Power Play Opportunities Against (PPOA). Total number of power play opportunities the opposing team had against them. Indicates how often the team was penalized, giving the opponent a man advantage.
  - **`pen_kill_pct`** (number, decimal) - Penalty Kill Percentage (PK%). Percentage of opposing power play opportunities successfully killed off. Higher percentages indicate better penalty-killing performance. Expressed as a decimal (e.g., 0.821).
  - **`pen_kill_pct`** (number, decimal) - Penalty Kill Percentage (PK%). Percentage of opposing power play opportunities successfully killed off. Higher percentages indicate better penalty-killing performance. Expressed as a decimal (e.g., 0.821).
  - **`opp_goals_sh`** (integer) - Short-Handed Goals Against (SHA). Total number of short-handed goals conceded by the team. Goals scored by the opposing team while on the penalty kill.
  - **`pen_min_per_game`** (number, decimal) - Penalties in Minutes Per Game (PIM/G). Average number of penalty minutes per game for the team. Reflects the team's discipline or lack thereof. Expressed as a decimal (e.g., 7.6).
  - **`pen_min_per_game_opp`** (number, decimal) - Opponent Penalties in Minutes Per Game (oPIM/G). Average number of penalty minutes per game for the opposing team. Reflects how often opponents were penalized against this team. Expressed as a decimal (e.g., 8.9).
  - **`shots`** (integer) - Shots on Goal (S). Total number of shots on goal taken by the team during the season. Reflects offensive activity.
  - **`shot_pct`** (number, decimal) - Shooting Percentage (S%). Percentage of shots on goal that resulted in goals. Calculated as (GF / S) * 100. Higher percentages indicate better shooting efficiency. Expressed as a decimal (e.g., 0.102).
  - **`shots_against`** (integer) - Shots Against (SA). Total number of shots on goal taken by opponents against the team. Reflects defensive pressure faced.
  - **`save_pct`** (number, decimal) - Save Percentage (SV%). Percentage of shots on goal stopped by the team's goaltenders. Calculated as 1 - (GA / SA). Higher percentages indicate better goaltending. Expressed as a decimal (e.g., 0.915).
  - **`shutouts`** (integer) - Shutouts (SO). Total number of games in which the team did not allow any goals. Reflects strong defensive and goaltending performances.

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/team_analytics_5_on_5_2022/
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
  - **`shot_pct_5on5`** (number, decimal) - Shooting Percentage (S%) (5-on-5). Percentage of shots on goal that were scored at 5-on-5. Reflects shooting efficiency. Expressed as a decimal (e.g., 0.087).
  - **`shot_pct_5on5`** (number, decimal) - Shooting Percentage (S%) (5-on-5). Percentage of shots on goal that were scored at 5-on-5. Reflects shooting efficiency. Expressed as a decimal (e.g., 0.087).
  - **`pdo`** (number, decimal) - Shooting % + Save % (PDO). Sum of Shooting Percentage and Save Percentage at 5-on-5. Used as an indicator of puck luck. Expressed as a decimal (e.g., 1.008).
  - **`corsi_for_5on5`** (integer) - Corsi For (CF) (5-on-5). Measures the total number of shot attempts (including shots on goal, missed shots, and blocked shots) generated by a team while playing at even strength (5-on-5). Measures offensive possession.
  - **`corsi_against_5on5`** (integer) - Corsi Against (CA) (5-on-5). Measures the total number of shot attempts (including shots on goal, missed shots, and blocked shots) directed at the team's own net while playing at even strength (5-on-5). Measures defensive pressure faced.
  - **`corsi_pct_5on5`** (number, decimal) - Corsi For Percentage (CF%) (5-on-5). Percentage of total shot attempts controlled by the team at 5-on-5. Above 50% indicates puck control dominance. Expressed as a decimal (e.g., 0.527).
  - **`fenwick_for_5on5`** (integer) - Fenwick For (FF) (5-on-5). Total number of unblocked shot attempts (shots + misses) by the team at 5-on-5. Like Corsi, but excludes blocked shots.
  - **`fenwick_against_5on5`** (integer) - Fenwick Against (FA) (5-on-5). Total number of unblocked shot attempts (shots + misses) allowed by the team at 5-on-5. Like Corsi, but excludes blocked shots.
  - **`fenwick_against_5on5`** (integer) - Fenwick Against (FA) (5-on-5). Total number of unblocked shot attempts (shots + misses) allowed by the team at 5-on-5. Like Corsi, but excludes blocked shots.
  - **`opp_chances_pp`** (integer) - Power Play Opportunities Against (PPOA). Total number of power play opportunities the opposing team had against them. Indicates how often the team was penalized, giving the opponent a man advantage.
  - **`pen_kill_pct`** (number, decimal) - Penalty Kill Percentage (PK%). Percentage of opposing power play opportunities successfully killed off. Higher percentages indicate better penalty-killing performance. Expressed as a decimal (e.g., 0.821).
  - **`pen_kill_pct`** (number, decimal) - Penalty Kill Percentage (PK%). Percentage of opposing power play opportunities successfully killed off. Higher percentages indicate better penalty-killing performance. Expressed as a decimal (e.g., 0.821).
  - **`opp_goals_sh`** (integer) - Short-Handed Goals Against (SHA). Total number of short-handed goals conceded by the team. Goals scored by the opposing team while on the penalty kill.
  - **`pen_min_per_game`** (number, decimal) - Penalties in Minutes Per Game (PIM/G). Average number of penalty minutes per game for the team. Reflects the team's discipline or lack thereof. Expressed as a decimal (e.g., 7.6).
  - **`pen_min_per_game_opp`** (number, decimal) - Opponent Penalties in Minutes Per Game (oPIM/G). Average number of penalty minutes per game for the opposing team. Reflects how often opponents were penalized against this team. Expressed as a decimal (e.g., 8.9).
  - **`shots`** (integer) - Shots on Goal (S). Total number of shots on goal taken by the team during the season. Reflects offensive activity.
  - **`shot_pct`** (number, decimal) - Shooting Percentage (S%). Percentage of shots on goal that resulted in goals. Calculated as (GF / S) * 100. Higher percentages indicate better shooting efficiency. Expressed as a decimal (e.g., 0.102).
  - **`shots_against`** (integer) - Shots Against (SA). Total number of shots on goal taken by opponents against the team. Reflects defensive pressure faced.
  - **`save_pct`** (number, decimal) - Save Percentage (SV%). Percentage of shots on goal stopped by the team's goaltenders. Calculated as 1 - (GA / SA). Higher percentages indicate better goaltending. Expressed as a decimal (e.g., 0.915).
  - **`shutouts`** (integer) - Shutouts (SO). Total number of games in which the team did not allow any goals. Reflects strong defensive and goaltending performances.

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/team_analytics_5_on_5_2022/TOR/
```
<a name="team_analytics_5_on_5_now"></a>
### 3.5 Get teams analytics 5 on 5 for the current season
- **Endpoint:** `/team_analytics_5_on_5_now/`
- **Method:** GET
- **Description:** Table presents advanced statistics for NHL teams , focusing on 5-on-5 play of all team for current season
- **Parameters:** No
- **Response:** JSON format
- **Schema table:**
  - **`ranker`** (integer) - Rank. The position of the team in the ranking based on their performance metrics.
  - **`team_name`** (string) - Team Name. The name of the NHL team.
  - **`abbreviation`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`playoff`** (string) - Indicator if the team made the playoffs that season (e.g., 'Yes', 'No).
  - **`shot_pct_5on5`** (number, decimal) - Shooting Percentage (S%) (5-on-5). Percentage of shots on goal that were scored at 5-on-5. Reflects shooting efficiency. Expressed as a decimal (e.g., 0.087).
  - **`shot_pct_5on5`** (number, decimal) - Shooting Percentage (S%) (5-on-5). Percentage of shots on goal that were scored at 5-on-5. Reflects shooting efficiency. Expressed as a decimal (e.g., 0.087).
  - **`pdo`** (number, decimal) - Shooting % + Save % (PDO). Sum of Shooting Percentage and Save Percentage at 5-on-5. Used as an indicator of puck luck. Expressed as a decimal (e.g., 1.008).
  - **`corsi_for_5on5`** (integer) - Corsi For (CF) (5-on-5). Measures the total number of shot attempts (including shots on goal, missed shots, and blocked shots) generated by a team while playing at even strength (5-on-5). Measures offensive possession.
  - **`corsi_against_5on5`** (integer) - Corsi Against (CA) (5-on-5). Measures the total number of shot attempts (including shots on goal, missed shots, and blocked shots) directed at the team's own net while playing at even strength (5-on-5). Measures defensive pressure faced.
  - **`corsi_pct_5on5`** (number, decimal) - Corsi For Percentage (CF%) (5-on-5). Percentage of total shot attempts controlled by the team at 5-on-5. Above 50% indicates puck control dominance. Expressed as a decimal (e.g., 0.527).
  - **`fenwick_for_5on5`** (integer) - Fenwick For (FF) (5-on-5). Total number of unblocked shot attempts (shots + misses) by the team at 5-on-5. Like Corsi, but excludes blocked shots.
  - **`fenwick_against_5on5`** (integer) - Fenwick Against (FA) (5-on-5). Total number of unblocked shot attempts (shots + misses) allowed by the team at 5-on-5. Like Corsi, but excludes blocked shots.
  - **`fenwick_against_5on5`** (integer) - Fenwick Against (FA) (5-on-5). Total number of unblocked shot attempts (shots + misses) allowed by the team at 5-on-5. Like Corsi, but excludes blocked shots.
  - **`opp_chances_pp`** (integer) - Power Play Opportunities Against (PPOA). Total number of power play opportunities the opposing team had against them. Indicates how often the team was penalized, giving the opponent a man advantage.
  - **`pen_kill_pct`** (number, decimal) - Penalty Kill Percentage (PK%). Percentage of opposing power play opportunities successfully killed off. Higher percentages indicate better penalty-killing performance. Expressed as a decimal (e.g., 0.821).
  - **`pen_kill_pct`** (number, decimal) - Penalty Kill Percentage (PK%). Percentage of opposing power play opportunities successfully killed off. Higher percentages indicate better penalty-killing performance. Expressed as a decimal (e.g., 0.821).
  - **`opp_goals_sh`** (integer) - Short-Handed Goals Against (SHA). Total number of short-handed goals conceded by the team. Goals scored by the opposing team while on the penalty kill.
  - **`pen_min_per_game`** (number, decimal) - Penalties in Minutes Per Game (PIM/G). Average number of penalty minutes per game for the team. Reflects the team's discipline or lack thereof. Expressed as a decimal (e.g., 7.6).
  - **`pen_min_per_game_opp`** (number, decimal) - Opponent Penalties in Minutes Per Game (oPIM/G). Average number of penalty minutes per game for the opposing team. Reflects how often opponents were penalized against this team. Expressed as a decimal (e.g., 8.9).
  - **`shots`** (integer) - Shots on Goal (S). Total number of shots on goal taken by the team during the season. Reflects offensive activity.
  - **`shot_pct`** (number, decimal) - Shooting Percentage (S%). Percentage of shots on goal that resulted in goals. Calculated as (GF / S) * 100. Higher percentages indicate better shooting efficiency. Expressed as a decimal (e.g., 0.102).
  - **`shots_against`** (integer) - Shots Against (SA). Total number of shots on goal taken by opponents against the team. Reflects defensive pressure faced.
  - **`save_pct`** (number, decimal) - Save Percentage (SV%). Percentage of shots on goal stopped by the team's goaltenders. Calculated as 1 - (GA / SA). Higher percentages indicate better goaltending. Expressed as a decimal (e.g., 0.915).
  - **`shutouts`** (integer) - Shutouts (SO). Total number of games in which the team did not allow any goals. Reflects strong defensive and goaltending performances.

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/team_analytics_5_on_5_now/
```
<a name="team_analytics_5_on_5_now/{abbreviation}"></a>
### 3.6 Get teams analytics 5 on 5 for the current season and specific team
- **Endpoint:** `/team_analytics_5_on_5_now/{abbreviation}/`
- **Method:** GET
- **Description:** Table presents advanced statistics for NHL teams , focusing on 5-on-5 play of a specific team for current season
- **Parameters:**
   - **`{abbreviation}`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format
- **Schema table:**
  - **`ranker`** (integer) - Rank. The position of the team in the ranking based on their performance metrics.
  - **`team_name`** (string) - Team Name. The name of the NHL team.
  - **`abbreviation`** (string) - Three-letter team abbreviation (e.g., "TOR", "MTL").
  - **`playoff`** (string) - Indicator if the team made the playoffs that season (e.g., 'Yes', 'No).
  - **`shot_pct_5on5`** (number, decimal) - Shooting Percentage (S%) (5-on-5). Percentage of shots on goal that were scored at 5-on-5. Reflects shooting efficiency. Expressed as a decimal (e.g., 0.087).
  - **`shot_pct_5on5`** (number, decimal) - Shooting Percentage (S%) (5-on-5). Percentage of shots on goal that were scored at 5-on-5. Reflects shooting efficiency. Expressed as a decimal (e.g., 0.087).
  - **`pdo`** (number, decimal) - Shooting % + Save % (PDO). Sum of Shooting Percentage and Save Percentage at 5-on-5. Used as an indicator of puck luck. Expressed as a decimal (e.g., 1.008).
  - **`corsi_for_5on5`** (integer) - Corsi For (CF) (5-on-5). Measures the total number of shot attempts (including shots on goal, missed shots, and blocked shots) generated by a team while playing at even strength (5-on-5). Measures offensive possession.
  - **`corsi_against_5on5`** (integer) - Corsi Against (CA) (5-on-5). Measures the total number of shot attempts (including shots on goal, missed shots, and blocked shots) directed at the team's own net while playing at even strength (5-on-5). Measures defensive pressure faced.
  - **`corsi_pct_5on5`** (number, decimal) - Corsi For Percentage (CF%) (5-on-5). Percentage of total shot attempts controlled by the team at 5-on-5. Above 50% indicates puck control dominance. Expressed as a decimal (e.g., 0.527).
  - **`fenwick_for_5on5`** (integer) - Fenwick For (FF) (5-on-5). Total number of unblocked shot attempts (shots + misses) by the team at 5-on-5. Like Corsi, but excludes blocked shots.
  - **`fenwick_against_5on5`** (integer) - Fenwick Against (FA) (5-on-5). Total number of unblocked shot attempts (shots + misses) allowed by the team at 5-on-5. Like Corsi, but excludes blocked shots.
  - **`fenwick_against_5on5`** (integer) - Fenwick Against (FA) (5-on-5). Total number of unblocked shot attempts (shots + misses) allowed by the team at 5-on-5. Like Corsi, but excludes blocked shots.
  - **`opp_chances_pp`** (integer) - Power Play Opportunities Against (PPOA). Total number of power play opportunities the opposing team had against them. Indicates how often the team was penalized, giving the opponent a man advantage.
  - **`pen_kill_pct`** (number, decimal) - Penalty Kill Percentage (PK%). Percentage of opposing power play opportunities successfully killed off. Higher percentages indicate better penalty-killing performance. Expressed as a decimal (e.g., 0.821).
  - **`pen_kill_pct`** (number, decimal) - Penalty Kill Percentage (PK%). Percentage of opposing power play opportunities successfully killed off. Higher percentages indicate better penalty-killing performance. Expressed as a decimal (e.g., 0.821).
  - **`opp_goals_sh`** (integer) - Short-Handed Goals Against (SHA). Total number of short-handed goals conceded by the team. Goals scored by the opposing team while on the penalty kill.
  - **`pen_min_per_game`** (number, decimal) - Penalties in Minutes Per Game (PIM/G). Average number of penalty minutes per game for the team. Reflects the team's discipline or lack thereof. Expressed as a decimal (e.g., 7.6).
  - **`pen_min_per_game_opp`** (number, decimal) - Opponent Penalties in Minutes Per Game (oPIM/G). Average number of penalty minutes per game for the opposing team. Reflects how often opponents were penalized against this team. Expressed as a decimal (e.g., 8.9).
  - **`shots`** (integer) - Shots on Goal (S). Total number of shots on goal taken by the team during the season. Reflects offensive activity.
  - **`shot_pct`** (number, decimal) - Shooting Percentage (S%). Percentage of shots on goal that resulted in goals. Calculated as (GF / S) * 100. Higher percentages indicate better shooting efficiency. Expressed as a decimal (e.g., 0.102).
  - **`shots_against`** (integer) - Shots Against (SA). Total number of shots on goal taken by opponents against the team. Reflects defensive pressure faced.
  - **`save_pct`** (number, decimal) - Save Percentage (SV%). Percentage of shots on goal stopped by the team's goaltenders. Calculated as 1 - (GA / SA). Higher percentages indicate better goaltending. Expressed as a decimal (e.g., 0.915).
  - **`shutouts`** (integer) - Shutouts (SO). Total number of games in which the team did not allow any goals. Reflects strong defensive and goaltending performances.

##### Example using
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
crashcrab.ddns.net/{YOUR_API_KEY}/season_summary_2021/
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
crashcrab.ddns.net/{YOUR_API_KEY}/season_summary_2021/TOR/
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
crashcrab.ddns.net/{YOUR_API_KEY}/season_summary_now/
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
crashcrab.ddns.net/{YOUR_API_KEY}/season_summary_now/TOR/
```
<a name="season_statistics_{year}"></a>
### 4.5 Get detail statistic season by year
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
crashcrab.ddns.net/{YOUR_API_KEY}/season_statistics_2022/
```
<a name="season_statistics_{year}/{abbreviation}"></a>
### 4.6 Get detail statistic season by year and specific team
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
crashcrab.ddns.net/{YOUR_API_KEY}/season_statistics_2022/TOR/
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
crashcrab.ddns.net/{YOUR_API_KEY}/season_statistics_now/
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
crashcrab.ddns.net/{YOUR_API_KEY}/season_statistics_now/TOR/
```
<a name="league_average_{year}"></a>
### 4.9 Get league average by year
- **Endpoint:** `/league_average_{year}/`
- **Method:** GET
- **Description:** League average for the specific season
- **Parameters:**
   - **`year`** (integer) - A dynamic prefix identifying a season or data set (e.g. "20112012", "20172018", "20232024"). This prefix is ​​part of the path and is used to identify the data table.
- **Response:** JSON format
- **Schema table:**
  - **`average_age`** (number, decimal) - Average Age (AvAge). Average age of team weighted by time on ice. Expressed as a decimal (e.g., 27.4).
  - **`games`** (integer) - Games Played (GP). Total number of games played by the team during the regular season.
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout.
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout.
  - **`losses_ot`** (integer) - Overtime/Shootout Losses (OL). Total number of games lost by the team in overtime or shootout (relevant from 2000 season onward).
  - **`points`** (integer) - Points (PTS). Total points accumulated by the team during the regular season. Teams earn 2 points for a win, 1 point for an overtime/shootout loss, and 0 points for a regulation loss.
  - **`points_pct`** (number, decimal) - Points Percentage (PTS%). The percentage of total possible points earned by the team. Calculated as PTS / (GP * 2). Useful for comparing teams with different numbers of games played. Expressed as a decimal (e.g., 0.671).
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
crashcrab.ddns.net/{YOUR_API_KEY}/league_average_2022/
```
<a name="league_average_now"></a>
### 4.10 Get league average for the current season
- **Endpoint:** `/league_average_now/`
- **Method:** GET
- **Description:** League average for the current season
- **Parameters:** No
- **Response:** JSON format
- **Schema table:**
  - **`average_age`** (number, decimal) - Average Age (AvAge). Average age of team weighted by time on ice. Expressed as a decimal (e.g., 27.4).
  - **`games`** (integer) - Games Played (GP). Total number of games played by the team during the regular season.
  - **`wins`** (integer) - Wins. Total number of games won by the team in regulation, overtime, or shootout.
  - **`losses`** (integer) - Losses. Total number of games lost by the team in regulation, overtime, or shootout.
  - **`losses_ot`** (integer) - Overtime/Shootout Losses (OL). Total number of games lost by the team in overtime or shootout (relevant from 2000 season onward).
  - **`points`** (integer) - Points (PTS). Total points accumulated by the team during the regular season. Teams earn 2 points for a win, 1 point for an overtime/shootout loss, and 0 points for a regulation loss.
  - **`points_pct`** (number, decimal) - Points Percentage (PTS%). The percentage of total possible points earned by the team. Calculated as PTS / (GP * 2). Useful for comparing teams with different numbers of games played. Expressed as a decimal (e.g., 0.671).
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
  - **`winner_team_abbrev`** (string) – Winner Team Abbreviation. Three-letter abbreviation for the team that won the game.
  - **`loser_team_name`** (string) – Loser Team Name. Full name of the team that lost the game.
  - **`loser_team_abbrev`** (string) – Loser Team Abbreviation. Three-letter abbreviation for the team that lost the game.
  - **`overtime`** (string) – Overtime. Indicates whether the game went to overtime, and may include additional info such as the number of overtime periods (e.g., "OT", "2OT", or NULL if decided in regulation).

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_playoff_series_result_2022/
```
<a name="league_playoff_series_result_{year}/{game_id}"></a>
### 5.2 Get playoff result by year and specific game
- **Endpoint:** `/league_playoff_series_result_{year}/{game_id}/`
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

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_playoff_series_result_2022/202205040LAK/
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

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_playoff_series_result_2022/date/2022-05-04/
```
<a name="league_playoff_series_result_now"></a>
### 5.4 Get playoff result for the current season
- **Endpoint:** `/league_playoff_series_result_now/`
- **Method:** GET
- **Description:** Table with results of playoff series games for the current season.
- **Parameters:** No
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

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_playoff_series_result_now/
```
<a name="league_playoff_series_result_now/{game_id}"></a>
### 5.5 Get playoff result for the current season and specific game
- **Endpoint:** `/league_playoff_series_result_now/{game_id}/`
- **Method:** GET
- **Description:** Table with results of playoff series games for the current season and specific game.
- **Parameters:**
     - **`game_id`** (string) – Game ID. Unique identifier for each playoff game (e.g. "202205040LAK").
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

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_playoff_series_result_now/202205040LAK/
```
<a name="league_playoff_series_result_now/date/{game_date}"></a>
### 5.6 Get playoff result for the current season and specific date
- **Endpoint:** `/league_playoff_series_result_now/date/{game_date}/`
- **Method:** GET
- **Description:** Table with results of playoff series games for a specific date for the current season.
- **Parameters:**
     - **`game_date`** (date) – Game Date. The date on which the playoff game was played (e.g., "2021-08-21").
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

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/league_playoff_series_result_now/date/2021-08-21/
```
