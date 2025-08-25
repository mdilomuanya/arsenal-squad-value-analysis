# Analysis of Arsenal FC Squad Value
![Arsenal_Banner](Assets/arsenal-crest-and-club-name2.png)
This project analyzes Arsenal’s wage bill efficiency by combining historic salary data, playing time, and a custom Game Impact Score (GIS) to evaluate player value relative to squad performance. Built with Python, Excel, and Tableau, the project answers five key questions surrounding changes in wage allocation over time, wage inefficiencies, player impact on performance impact, and alignment between wages and contribution, concluding with recommendations compared to Arsenal’s real-world contract decisions.
### Questions Answered
1. How has the average cost/minute played changed over time?
2. How much of the wage bill is wasted on underused players?
3. Who is overpaid relative to minutes?
5. Which players have the biggest impact on games (via GIS)?
6. Does impact align with wages—who are bargains vs inefficiencies?

---

## Tools and Technologies
- **Python** – Programmatic data scraping (`selenium`, `pandas`)
- **Excel** – For data cleaning, transformation, and exports
- **Tableau** – For interactive dashboards, visual storytelling, GIS creation using table calculations

---

## Project Workflow

### 1. Python: Data Collection & Enrichment
Used the selenium and pandas libraries to:
- Pull wage tables by season (2020/21→2024/25) from Capology
- Pull playing-time and impact stats from FBref (minutes, PPG/PPM, on–off xG context)
- Put them into separate data frames and export them as CSV files

**Output:** Two enriched CSV files (`spotify_enriched.csv`) with fields like `main_artist`, `artist_genres`, `artist_popularity`, and `streams`.

### 2. Excel: Cleaning & Harmonization
Using excel:
- Normalized names across datasets
- Cleaned NULLs and empty rows
- Created a unique key for each player for each season
- Used VLOOKUP to create a single table with the relevant data

**Output:** A clean excel table `Spotify_Project_MySQL.sql` 

### 3. Tableau: Game Impact Score Creation
Built table calculations in Tableau to create a Game Impact Score (GIS) mertic, weighting:
- Points Per Game (PPG)
- On-Off xG impact (team performance with vs without player)
- Highlight tables of regional superstars with localized success
Used Tableau normalization (percentiles) to compare across players/seasons
Created calculated fields and parameter controls to test different weightings

**Output:** Dynamic GIS field + normalized scores within Tableau workbooks


### 4. Tableau: Data Visualization
Final visualizations were built in Tableau (`Spotify_Tableau_Final.twb`) to visually answer the five research questions:
- Wage/Minute Over Time → tracked wage efficiency trends across seasons
- Overpaid vs Minutes → highlighted wages spent on underused players
- Wasted Wage Bill → compared total vs wasted wages by year
- Game Impact Score (GIS) → identified top contributors vs low-impact players
- Wages vs Impact → quadrant plot of bargains, justified earners, and inefficiencies

---
