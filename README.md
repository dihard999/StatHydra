# :crab:CrashCrab API
This application is a powerful API for sports analytics and match prediction, leveraging state-of-the-art machine learning algorithms. Designed for enthusiasts, analysts, and developers. With its robust and scalable architecture, the API offers seamless integration and real-time predictions, making it an essential tool for anyone seeking data-driven insights into the world of sports.  
---
---
# Table of Data
1. [Base URL](#base-url)
2. [Player](#player)
3. [Team](#team)
4. [Season](#season)  
   4.1 [Get all season statistic summary(except for the current season)](#team_all_season_summary)
5. [Game](#game)
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
## Team
---
## Season  
<a name="team_all_season_summary"></a>
### Get all season statistic summary(except for the current season)
- **Endpoint:** `/team_all_season_summary/`
- **Method:** GET
- **Description:** Retrieves aggregated statistics for all teams across all seasons they participated in the NHL.
- **Parameters:** No
- **Request Parameters:**
  - **`/team_all_season_summary/{abbreviation}`** (query, string, optional) - General statistics of a specific team for all seasons (except for the current season). Three-letter team abbreviation (e.g., "TOR", "MTL").
- **Response:** JSON format

##### Example using
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/api/v1/team_all_season_summary/
```
```bash
crashcrab.ddns.net/{YOUR_API_KEY}/api/v1/team_all_season_summary/TOR
```
---
## Game
