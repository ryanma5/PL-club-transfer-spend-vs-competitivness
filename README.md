# PL Club Transfer Spend vs Competitiveness ⚽ 🏆

[Tableau Visualization](https://public.tableau.com/views/PremierLeague2020-2024/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

## Background
The English Premier League is considered one of the most competitive leagues in the world, where clubs spend millions of pounds every transfer window on acquiring top football talents across the world. I want to investigate how much effect transfer spendings have on a club’s competitiveness. 

I want to create a visualization that plots the relationship between Premier League Clubs’ net transfer spend the past five seasons, and their competitiveness, represented by their total points secured the past five seasons.

## Data Sources
-	Transfer spending data: [transfermarkt.com](https://www.transfermarkt.us/premier-league/fuenfjahresvergleich/wettbewerb/GB1)
-	League points data: [fbref.com](https://fbref.com/en/comps/9/2020-2021/2020-2021-Premier-League-Stats) <sup>league table for one season</sup>

## Methodology

### Data Collection (Python)
- Scrapped and compiled transfer spending data from transfermarkt.com using BeautifulSoup library
- Scrapped and compiled league points data from transfermarkt.com

### Data Cleaning/Manipulation (Python)
-	Standardized club names across datasets for accurate merging
-	Merged datasets to create a complete list of Premier League Clubs, their respective cumulative league points, and transfer spending, across five seasons
-	Removed teams who were in the premier league for < 3 years to only include teams who have consistently competed in the top flight

### Visualization [Tableau Link](https://public.tableau.com/views/PremierLeague2020-2024/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
-	Created a scatter plot of Net spend vs total cumulative points of clubs on tableau

## Findings
-	P-value of 0.025 (<0.05) suggests that It’s very likely there exists a correlation between a club’s net transfer spend and their competitiveness in the Premier League
-	R-squared of 0.28 means only 28% of the variance is explained by net transfer spend, a significant of portion of variance is explained by other factors (e.g. Youth facility investments, wages, manager hire spending etc.)

## Next Steps
-	Investigate and incorporate additional variables (e.g. Youth facility investments, wages, manager hire spending etc.) to improve explanatory power of the model

## Repository Structure

| File | Content |
| ------ | ------ |
| [PL_5_year_league_table.ipynb](PL_5_year_league_table.ipynb) | Jupyter notebook for scrapping league points data from fbref.com |
| [PL_5_year_net_spend.ipynb](PL_5_year_net_spend.ipynb) | Jupyter notebook for scrapping net transfer spend data from transfermarkt.com |
| [Best_run_PL_clubs.ipynb](Best_run_PL_clubs.ipynb) | Jupyter notebook for data cleaning/manipulation and merging of datasets |








