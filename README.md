# Introduction

## Project Setup

Used Python 3.13 and the following libraries:

- pandas version: 2.2.3
- numpy version: 2.2.5
- matplotlib version: 3.10.1
- seaborn version: 0.13.2
- sqlalchemy version: 2.0.40

## Data Source

The Starbucks rewards dataset is provided as part of the project.

This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks.

## Project Structure

```bash
├── data/                             # Contains the dataset files
├── docs/                             # Files used for GitHub Pages post containing the report
├── 1_data_ingestion.ipynb            # Python notebook used to ingest the JSON files provided into sqlite tables
├── 2_eda.ipynb                       # Python notebook used for basic data analysis
├── 3_eda_user_journey.ipynb          # Python notebook used for figuring out combinations of users with the event types
├── 4_user_group_aggregations.ipynb   # Python notebook used for additional data analysis. Lead to the development of 5_completion_percentages.ipynb
├── 5_completion_percentages.ipynb    # Python notebook used to calculate the offer completion percentages for final results
└── README.md                         # Project documentation
```

## Project description

This project is a simple analysis of the simulated Starbucks rewards data set. I have left my data analysis scripts so as to allow for traversal of my logic, but the only notebooks necessary for producing the final results are `1_data_ingestion.ipynb` and `5_completion_percentages.ipynb`. Additionally, the 3 json files must be provided in the data folder. This is also where the `starbucks_data.db` will be created when running `1_data_ingestion.ipynb`. The `docs/images` folder contains graphs saved in my analysis and for the results.

## Project Results

The full report is available at in my GitHub Pages [post](https://meeby280.github.io/UdacityDataScienceProject4/2025/04/02/Project-4.html). To summarize, by creating a customer journey from receiving and offer to offer completion, across most user demographics and offer types, the most likely to be completed are discount offers.

## References used

- https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.combine_first.html
  - Used to coalesce the offer id values within the interactions value column
- https://matplotlib.org/stable/gallery/pie_and_polar_charts/pie_features.html
  - Used to create the pie charts.
- https://stackoverflow.com/questions/74623054/get-the-current-version-of-the-current-package-in-python
  - For getting versions of the packages used.
