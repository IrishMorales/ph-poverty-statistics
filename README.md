# Philippine Poverty Statistics
An exploratory data analysis of Philippine poverty data. Data includes 1991-2015 data, appended FIES 2018 & 2021 data, and 2024 & 2027 poverty estimates personally calculated using ARIMA.

### 🔶 File List
| Filename                    | Description                                                                                       |
|-----------------------------|---------------------------------------------------------------------------------------------------|
| .gitignore                  | Utility file to avoid pushing temporary local files                                               |
| 2018_FIES_processed.csv     | 2018 FIES data manually formatted in Google Sheets to match the main dataset                      |
| 2021_FIES_processed.csv     | 2021 FIES data manually formatted in Google Sheets to match the main dataset                      |
| README.md                   | This file you're reading! :)                                                                      |
| Slide Deck.pdf              | Presentation slides of key insights found from EDA                                                |
| ph-poverty-statistics.ipynb | Jupyter notebook containing all code for data preparation and EDA                                 |
| pov_incidence_change.csv    | Data for poverty incidence change between 1991 & 2021, generated from ph-poverty-statistics.ipynb |
| povstat_analysis.twb        | All Tableau data visualizations and dashboards                                                    |
| povstat_processed.csv       | 1991-2015 data provided by Thinking Machines                                                      |
| povstat_until_2021.csv      | 1991-2021 data from povstat_processed.csv + 2018_FIES_processed.csv + 2021_FIES_processed.csv, generated from ph-poverty-statistics.ipynb  |
| povstat_until_2027.csv      | 1991-2027 data from povstat_until_2021.csv + 2024 & 2027 forecasts, generated from ph-poverty-statistics.ipynb                             |

### 🔶 Interactive Dashboards
All data visualizations created of the dataset can be found here. Please click the links for the interactive versions, as the ones shown below are screenshots only.
- [Philippine Poverty Data Explorer](https://bit.ly/PH-poverty-explorer-1) - For exploring the dataset
  ![image](https://user-images.githubusercontent.com/42305156/233829651-5aa2d36f-606b-45d2-bc93-12375247bec9.png)
- [Philippine Poverty Statistics](https://bit.ly/PH-poverty-stat-2) - Key insights from EDA
  ![pov_statistics-1](https://user-images.githubusercontent.com/42305156/233829906-f6194ea1-252e-4210-a4e0-7836db1d5ab0.png)

### 🔶 Data Sources
- **1991-2015 Data** - Provided by Thinking Machines
- **FIES 2018 & 2021 Data** - "2021 Full Year Official Poverty Statistics Tables" from https://psa.gov.ph/poverty-press-releases/nid/167972
Unfortunately, the 2021 data here is from the preliminary 2021 FIES results, as I could not find a full and official release of the finalized 2021 data with these variables. I then created the .csv files manually to match the formatting of this dataset. For easy viewing, I copied the original attachment data [here](https://docs.google.com/spreadsheets/d/1vS7aF0Vl632l7dWEUgs5GxfWZsmMmvFY/edit?usp=sharing&ouid=100450481071067541565&rtpof=true&sd=true). I then cleaned and reformatted the 2018 & 2021 data [here](https://docs.google.com/spreadsheets/d/1GCU--tzB7GWSx1Uk7ddlA7EsoQ6rNp91_UUDbleZ0nI/edit?usp=sharing). The final processed .csv files are in this GitHub repo ([2018](https://github.com/IrishMorales/ph-poverty-statistics/blob/b94819039b8f141cd2bfc3b667d748418cfb5f2a/2018_FIES_processed.csv), [2021](https://github.com/IrishMorales/ph-poverty-statistics/blob/master/2021_FIES_processed.csv)).
- **2024 & 2027 Data** - Personally forecasted using Autoregressive Integrated Moving Average (ARIMA). Process and full details seen in the [.ipynb file](https://github.com/IrishMorales/ph-poverty-statistics/blob/b94819039b8f141cd2bfc3b667d748418cfb5f2a/ph-poverty-statistics.ipynb). *Caveats:* Forecasts are likely not very accurate due to very few data points for the model to train on and data may be slightly skewed due to the 2021 pandemic. Overall, however, the forecast can at least give us at least some general idea of developments in poverty for the coming years.
