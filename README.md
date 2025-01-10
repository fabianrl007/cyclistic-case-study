# cyclistic-case-study
# Cyclistic Bike-Share Analysis: Converting Casual Riders to Annual Members

## Overview

This repository contains the R code and data analysis for a case study focused on Cyclistic, a fictional bike-share company based in Chicago. The goal of this project is to analyze historical bike trip data to identify key differences in usage patterns between casual riders and annual members. The insights derived from this analysis are then used to develop data-driven recommendations for targeted marketing strategies aimed at converting casual riders into annual members.

## Business Problem

Cyclistic's marketing strategy has historically relied on broad appeal and general awareness campaigns. However, the finance team has determined that annual members are significantly more profitable than casual riders. The marketing team, therefore, wants to focus on maximizing the number of annual memberships. This project aims to understand how casual riders and annual members use Cyclistic bikes differently to inform marketing strategies for conversion.

## Data Source

The data for this analysis is sourced from Motivate International Inc., the operator of the Divvy bike-share system in Chicago, which is the system that Cyclistic uses for their own. The datasets used in this case study include Divvy's trip data from the first quarter of 2019, and the first quarter of 2020. The data is publicly available under the Divvy Data License Agreement: [https://divvybikes.com/data-license-agreement](https://divvybikes.com/data-license-agreement)

**Data Files:**

*   **Divvy_Trips_2019_Q1.csv:** Bike trip data for Q1 2019.
*   **Divvy_Trips_2020_Q1.csv:** Bike trip data for Q1 2020.

## Tools and Libraries

This analysis was conducted using R and the following libraries:

*   **tidyverse:** For data manipulation, analysis, and visualization (including `dplyr`, `ggplot2`, `readr`, `tidyr`, and `lubridate`).
*   **zoo:** For handling missing values.
*   **conflicted:** For managing function conflicts.

## Analysis Process

The analysis followed the steps of the data analysis process:

1.  **ASK:** Defined the business problem, identified key stakeholders, and formulated a clear statement of the business task.
2.  **PREPARE:** Located, downloaded, and stored the data. Inspected the data structure, assessed data integrity, and identified potential data issues.
3.  **PROCESS:** Cleaned and transformed the data using R. This included:
    *   Removing unnecessary columns.
    *   Converting data types to appropriate formats (e.g., `started_at`, `ended_at` to `POSIXct`).
    *   Combining data frames.
    *   Recoding `member_casual` column.
    *   Adding calculated columns (`date`, `month`, `day`, `year`, `day_of_week`, `ride_length_seconds`).
    *   Handling missing values (imputation and removal).
    *   Removing "bad" data.
4.  **ANALYZE:** Performed descriptive and comparative analysis to identify trends and relationships. Calculated key metrics such as total rides, average ride length, and day-of-week usage patterns.
5.  **SHARE:** Created visualizations using `ggplot2` to communicate findings effectively. These visualizations are included in the Medium post (link below).
6.  **ACT:** Developed data-driven recommendations for the marketing team to convert casual riders into annual members.

## Key Findings

*   Casual riders take significantly longer rides than annual members (average ride length of 5627 seconds vs. 786 seconds).
*   Casual riders use Cyclistic bikes more on weekends (Saturday and Sunday) compared to members, who use the bikes more consistently throughout the week.
*   There is an unusually high average ride duration for casual riders on Thursdays, which warrants further investigation.
*   Members account for a much larger proportion of total rides (77.4%) compared to casual riders (22.6%).

## Recommendations

1.  **Implement Targeted Weekend Promotions for Casual Riders:** Offer discounts, limited-time offers, or special perks to incentivize weekend riders to become annual members.
2.  **Emphasize Leisure and Recreational Use in Marketing Materials:** Showcase the use of Cyclistic bikes for fun and exploration in marketing campaigns.
3.  **Investigate and Address the Thursday Anomaly:** Conduct further research to understand the reasons behind the high average ride duration for casual riders on Thursdays.

## Further Analysis

*   Hourly usage patterns analysis.
*   Station-level analysis.
*   Geographic analysis (if location data were available).
*   Collection of demographic data.
*   User surveys to gather qualitative data.
*   A/B testing of marketing campaigns.
*   Cohort analysis of casual riders.

## Repository Contents

*   **Cyclistic Bike-Share Analysis.html:** The R script containing the complete data analysis code.
*   **README.md:** This file, providing an overview of the project.
*   **Data:**: Data: The data used in this project is publicly available from Divvy Bikes at:[(https://divvy-tripdata.s3.amazonaws.com/index.html)].


## How to Run the Code

1.  Clone this repository to your local machine.
2.  Make sure you have R and RStudio installed.
3.  Install the required R packages: `install.packages(c("tidyverse", "lubridate", "zoo", "conflicted"))`
4.  Open the `cyclistic_analysis.R` script in RStudio.
5.  Update the file paths in the `read_csv()` functions to match the location of the data files on your system.
6.  Run the entire script.

## Author

\[Fabian Rosales]

## Contact

\[fabianrl007@gmail.com]

## License

This project is for educational purposes. The original data is available under the Divvy Data License Agreement: [https://divvybikes.com/data-license-agreement](https://divvybikes.com/data-license-agreement)

**Link to Medium Post:**

\[https://medium.com/p/36e87aee35bb/edit]
