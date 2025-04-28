# Introduction

## Project Setup

Used Python 3.13 and the following libraries:

```bash
pip install pandas numpy matplotlib seaborn
```

## Data Source

The Starbucks rewards dataset is provided as part of the project.

This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks.

## Project Structure

```bash
├── data/                           # Contains the dataset files
├── docs/                           # Files used for GitHub Pages post containing the report
├── data_ingestion.ipynb            # Python notebook used to ingest the JSON files provided into sqlite tables
├── eda.ipynb                       # Python notebook used for basic data analysis
├── eda_user_journey.ipynb          # Python notebook used for figuring out combinations of users with the event types
├── completion_percentages.ipynb    # Python notebook used to calculate the offer completion percentages for final results
└── README.md                       # Project documentation
```

## Project description

This project is a simple analysis of the simulated Starbucks rewards data set.
