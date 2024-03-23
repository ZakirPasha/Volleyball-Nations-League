# VNL 2021-2023 Dataset Collection

This project is dedicated to assembling a comprehensive dataset covering the Volleyball Nations League (VNL) from 2021 to 2023. The dataset encompasses detailed roster information and individual player statistics, meticulously gathered through web scraping techniques using Python 3, BeautifulSoup, and Selenium.

## Overview

The dataset is structured into four primary CSV files, each offering a deep dive into the rosters and performance metrics of both men's and women's teams across the specified seasons. This project aims to provide a robust foundation for analysis, enabling insights into team dynamics, player development, and performance trends within international volleyball competitions.

## Dataset Files

- `df_mens_rosters_21_23.csv`: Men's team rosters, including player demographics and yearly statistics.
- `df_mens_indv_21_23.csv`: Individual men's player statistics, detailing performance in various match aspects.
- `df_womens_rosters_21_23.csv`: Women's team rosters, mirroring the men's roster structure.
- `df_womens_indv_21_23.csv`: Individual women's player statistics, across similar performance metrics.

## Kaggle Dataset

The dataset is available for download and exploration on Kaggle at the following link:

[VNL 2021-2023 Dataset on Kaggle](https://www.kaggle.com/datasets/zakirpasha/vnl-21-23)

## Methodology

This project involved sophisticated web scraping techniques to extract HTML and JavaScript-based tables from the official VNL website. Key tools and libraries used include:

- **Python 3**: The primary programming language for scripting and data manipulation.
- **BeautifulSoup**: Utilized for parsing HTML content and extracting data from static web pages.
- **Selenium**: Employed to interact with and scrape data from JavaScript-generated dynamic tables.

## Considerations and Challenges

- **Country IDs**: Each team's data was accessed via unique country IDs in the URL, which changed annually. A systematic approach was developed to loop through each team's data per year based on these IDs.
- **Player Age Discrepancies**: The age data was only accurate for 2023; thus, a function was implemented to deduce the correct age for players in 2021 and 2022.
- **Dynamic Data Extraction**: While BeautifulSoup efficiently handled static roster data, the dynamic nature of individual player statistics required the use of Selenium. This was particularly challenging for extracting match-by-match performance stats, necessitating a loop through each player and year for each statistic category.
