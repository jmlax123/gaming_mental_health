# Gaming and Mental Health Analysis

A data analysis researching the impacts of gaming addiction severity on academic performance, physical health, lifestyle habits, and social isolation across different demographics, platforms, and genres.

## Summary

### Socialization and Sleep Quality
* **Social and Sleep Deprivation:** Higher gaming addiction levels strongly correlate with a significant decline in social interaction and sleep quality. Time spent gaming directly cannibalizes these essential activities.

### Platform, Genre, & Finances
* **Addictive Genres:** RPGs and Battle Royale genres were seen to have higher rates of addiction than other genres mentioned in the data.
* **Console Vulnerability:** Playing on console seemed correlate with higher addiction severity vs. playing on other platforms.
* **Financial Uniformity:** Monthly spending on gaming was not affected by higher addiction severity.
* **PlayStation & SQL Insights:** A database CTE reveals that PlayStation has the highest percentage of highly addicted players (severity ≥ 3), though it has a smaller sample size. Action, MMO, and Shooter genres on PlayStation show the highest average addiction scores.
* **A Surprising Find: Web Publishing:** Merging the datasets uncovered a highly addictive niche classified under "Web Publishing," featuring endless, low-barrier gameplay loops.
* **Developers With Most Addictive Games:** High addiction scores showed up heavily around specific developers like KOMODO (*Visual Novel Maker*), Epic Games (*Fortnite*), and Respawn Entertainment (*Apex Legends*).

### Gaming Behavior
* **Playtime** Total weekly playtime does not correlate to higher addiction severity, proving that it is possible to game for several hours without adopting addictive behaviors.
* **Physical Pain:** Higher rates of addiction severity correlate directly with increased physical pain that results from excessive gaming.

### The Social Isolation Feedback Loop
The data reveals a strong correlation between social isolation and severe gaming addiction. While it is not completely clear which causes the other, the data points to a reinforcing feedback loop:
1. High gaming addiction leads to greater social isolation.
2. The resulting isolation drives individuals deeper into gaming.
3. This loop continues, regardless of whether the isolation or the addiction manifested first.

## SQL Database & Schema 
*Database:* The data has been structured into a local SQLite database (`gaming_mh_tables.db`) composed of five core tables:
* `survey_responses`: Contains psychological, behavioral, and physical health metrics.
* `games_catalog`: Standardizes game titles, developers, and publishers.
* `game_platforms`: Maps catalog items explicitly to Steam, PlayStation, or Xbox.
* `game_genres`: Contains exploded, cleaned, and standardized multi-categorical genre listings.
* `gamer_dem`: Isolates anonymized demographic profiles (age, gender, occupation).

*Schema:* Separating genres and platforms into distinct bridge tables allowed for a cleaner database and prevents duplicate survey row multiplication during SQL joins. This guarantees that aggregate counts and averages remain completely accurate across many-to-many dimensional connections.

## Data Anomalies & Clean Mappings
To allow successful relational joins between the messy survey fields and the clean platform databases, a targeted text-translation mapping dictionary resolved the following major name discrepancies:
* `cs:go` --> `counter-strike: global offensive`
* `civilization vi` --> `sid meier's civilization vi`
* `final fantasy xiv` --> `final fantasy xiv online`

*Note: Non-Steam PC titles or unsupported mobile games (such as Starcraft II, World of Warcraft, and Clash of Clans) without a platform catalog match default cleanly to `N/A` rows.*

## Setup and Installation

### Prerequisites
* Python 3.12+
* Git Bash (for Windows users)
* And/or VS Code terminal

### How to Use
1. Clone the repository and navigate to your project directory:
   ```bash
   cd /e/mlax/Projects/gaming_mental_health
   ```
2. Activate the pre-configured virtual environment:
   ```bash
   source venv/Scripts/activate
   ```
3. Install the required analytics packages:
   ```bash
   pip install -r requirements.txt
   ```

## Data Sources
- Gaming Mental Health CSV file (provided in `Gaming_Mental_Health_Data/`)
- Gaming Profiles 2025 CSV files (provided in 'Gaming_Profiles_Data/')
- Enriched data using the primary (https://www.kaggle.com/datasets/artyomkruglov/gaming-profiles-2025-steam-playstation-xbox) Gaming Profiles 2025 dataset published by Artyom Kruglov on Kaggle.

## Author
Mickey Lax

## Dataset Access
Due to GitHub file size limitations, the 3 GB+ raw datasets (`Gaming_Profiles_Data`) are hosted externally. 

1. Download the raw data from the **[Google Drive Link](https://drive.google.com/file/d/1JAqHtTKaZrV64L2-z6M2DY9XA5PSEP8K/view?usp=drive_link)**.
2. Extract the contents into a folder named `Gaming_Profiles_Data/` in the root directory of this project.
3. Run the notebooks as normal.


