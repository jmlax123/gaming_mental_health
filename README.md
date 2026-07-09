# Gaming and Mental Health Analysis

A data analysis researching the impacts of gaming addiction severity on academic performance, physical health, lifestyle habits, and social isolation across different demographics, platforms, and genres.

## Summary

### Socialization and Sleep Quality
* **Social and Sleep Deprivation:** Higher gaming addiction levels strongly correlate with a significant decline in social interaction and sleep quality. Time spent gaming directly cannibalizes these essential activities.

### Platform, Genre, & Finances
* **Addictive Genres:** RPGs and Battle Royale genres were seen to have higher rates of addiction than other genres mentioned in the data.
* **Console Vulnerability:** Playing on console seemed correlate with higher addiction severity vs. playing on other platforms.
* **Financial Uniformity:** Monthly spending on gaming was not affected by higher addiction severity.

### Gaming Behavior
* **Playtime** Total weekly playtime does not correlate to higher addiction severity, proving that it is possible to game for several hours without adopting addictive behaviors.
* **Physical Pain:** Higher rates of addiction severity correlate directly with increased physical pain that results from excessive gaming.

### The Social Isolation Feedback Loop
The data reveals a strong correlation between social isolation and severe gaming addiction. While it is not completely clear which causes the other, the data points to a reinforcing feedback loop:
1. High gaming addiction leads to greater social isolation.
2. The resulting isolation drives individuals deeper into gaming.
3. This loop continues, regardless of whether the isolation or the addiction manifested first.

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
   pip install pandas matplotlib seaborn requests ipykernel
   ```

## Data Sources
- Gaming Mental Health CSV file (provided in `Gaming_Mental_Health_Data/`)
- Gaming Profiles 2025 csv files (provided in 'Gaming_Profiles_Data/')

## Author
Mickey Lax

## 📊 Dataset Access
Due to GitHub file size limitations, the 3 GB+ raw datasets (`Gaming_Profiles_Data`) are hosted externally. 

1. Download the raw data from the **[Google Drive Link](https://drive.google.com/file/d/1JAqHtTKaZrV64L2-z6M2DY9XA5PSEP8K/view?usp=drive_link)**.
2. Extract the contents into a folder named `Gaming_Profiles_Data/` in the root directory of this project.
3. Run the notebooks as normal.


