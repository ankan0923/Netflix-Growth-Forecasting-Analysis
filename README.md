# Netflix Content Analysis and Predictive Analytics Using Historical Data

## Executive Summary

This project analyzes Netflix's content catalog to understand content distribution, growth trends, audience targeting, and future content expansion. Using historical Netflix title data, exploratory data analysis, statistical testing, and forecasting models were applied to identify patterns and predict future content additions.

The dataset originally contained 8,807 records. After cleaning missing values and removing incomplete records, 8,790 records remained for analysis. The project demonstrates an end-to-end data analytics workflow including data cleaning, exploratory analysis, statistical testing, and predictive modeling.


# 1. Introduction

Netflix is one of the world's largest streaming platforms with a vast catalog of movies and television shows. Understanding content trends helps identify business strategies, audience preferences, and future growth opportunities.

### Project Objectives

* Analyze Netflix content distribution.
* Identify trends in content growth.
* Explore country and genre contributions.
* Perform statistical analysis and hypothesis testing.
* Forecast future Netflix content additions using predictive models.


# 2. Data Cleaning and Preprocessing

The dataset contained missing values in several columns including:

* Director
* Cast
* Country
* Date Added
* Rating
* Duration

Data cleaning steps included:

* Missing categorical values replaced with "Unknown".
* Records with critical missing information removed.
* Date fields converted into datetime format.
* New features created:

  * Year Added
  * Month Added
  * Country Split
  * Genre
  * Gap (Year Added - Release Year)

### Final Dataset

* Original Records: 8,807
* Clean Records: 8,790


# 3. Exploratory Data Analysis

## Content Type Distribution

Netflix content is heavily dominated by movies.

| Type     | Count | Percentage |
| -------- | ----- | ---------- |
| Movies   | 6,126 | 69.69%     |
| TV Shows | 2,664 | 30.31%     |

### Insight

Movies represent nearly 70% of the Netflix catalog, indicating that Netflix relies heavily on film-based content.


## Country Analysis

Top contributing countries:

| Country        | Titles |
| -------------- | ------ |
| United States  | 3,681  |
| India          | 1,046  |
| United Kingdom | 805    |
| Canada         | 445    |

### Insight

The United States remains Netflix's primary content source. India is the second-largest contributor, highlighting Netflix's investment in international markets.


## Content Growth Over Time

Netflix content additions increased rapidly after 2015.

Yearly additions:

* 2016: 426
* 2017: 1,185
* 2018: 1,648
* 2019: 2,016 (Peak)
* 2020: 1,879
* 2021: 1,498

### Insight

The platform experienced explosive growth between 2016 and 2019, with 2019 being the strongest content acquisition year.


## Rating Analysis

Most common ratings:

| Rating | Count |
| ------ | ----- |
| TV-MA  | 3,205 |
| TV-14  | 2,157 |
| TV-PG  | 861   |
| R      | 799   |

### Insight

Netflix primarily targets mature audiences, with TV-MA and TV-14 representing over half of all content.


## Genre Analysis

Most popular genres:

| Genre                  | Count |
| ---------------------- | ----- |
| International Movies   | 2,752 |
| Dramas                 | 2,426 |
| Comedies               | 1,674 |
| International TV Shows | 1,349 |

### Insight

International content plays a critical role in Netflix's global strategy.


## Duration Analysis

### Movies

Movie duration statistics:

* Mean: 99.58 minutes
* Median: 98 minutes
* Standard Deviation: 28.28 minutes
* Most Common Duration: 90 minutes

### TV Shows

Season statistics:

* Mean: 1.75 seasons
* Median: 1 season
* Maximum: 17 seasons

### Insight

Most Netflix TV shows contain only one season, while movies typically last around 100 minutes.


# 4. Statistical Analysis

## Hypothesis Test 1

### Do movie durations differ across rating categories?

ANOVA Result:

* F Statistic = 98.11
* P-value < 0.001

### Conclusion

Movie durations vary significantly across different rating categories.

## Hypothesis Test 2

### Is the proportion of Movies and TV Shows equal?

Chi-Square Test:

* Statistic = 1363.53
* P-value < 0.001

### Conclusion

Movies and TV Shows are not equally represented. Movies dominate the platform.


## Hypothesis Test 3

### Has Netflix added more content after 2017?

T-Test:

* T Statistic = -12.91
* P-value = 2.13e-08

### Conclusion

Netflix significantly increased content additions after 2017.


# 5. Additional Business Insights

### Content Freshness

64.30% of all titles were released within the previous five years.

### Gap Analysis

Average gap between release and Netflix addition:

| Type    | Average Gap |
| ------- | ----------- |
| Movie   | 5.73 years  |
| TV Show | 2.30 years  |

### Insight

TV Shows are added much faster than Movies.

### Newer Content Analysis

Average release year:

* Movies: 2013
* TV Shows: 2017

TV Shows are generally newer than Movies.


# 6. Predictive Analytics

## Linear Regression Forecast

Predicted content additions:

| Year | Forecast |
| ---- | -------- |
| 2022 | 1,895    |
| 2023 | 2,064    |
| 2024 | 2,233    |
| 2025 | 2,402    |

### Model Performance

* MAE = 572.74
* RMSE = 657.78
* R² = -8.01

### Observation

Linear Regression does not adequately capture Netflix's content growth pattern.


## ARIMA Forecast

Predicted additions:

| Year | Forecast |
| ---- | -------- |
| 2022 | 1,226    |
| 2023 | 1,072    |
| 2024 | 985      |
| 2025 | 937      |
| 2026 | 909      |

### Observation

ARIMA predicts a gradual decline in content additions, suggesting Netflix may be approaching a mature growth stage.


## Prophet Forecast

Prophet forecasting model was trained successfully and used to model long-term growth trends.

### Observation

Prophet provides a flexible forecasting framework capable of handling trend changes and long-term business forecasting.


# 7. Business Recommendations

1. Continue investing in international content, which represents a major portion of the catalog.
2. Expand high-performing genres such as International Movies, Dramas, and Comedies.
3. Focus on TV Show production since they are added faster and are generally newer.
4. Monitor content acquisition trends as recent forecasts suggest slower growth compared to the rapid expansion period of 2016–2019.
5. Utilize forecasting models to optimize future content acquisition strategies.


# 8. Conclusion

The analysis reveals that Netflix's growth has been driven primarily by movies, international content, and mature-audience programming. Content additions accelerated dramatically after 2016 and peaked in 2019. Statistical testing confirmed significant differences across ratings, content types, and growth periods.

Predictive modeling suggests that future content growth may stabilize rather than continue the rapid expansion observed during Netflix's peak acquisition years. These findings provide valuable insights into Netflix's content strategy and future growth opportunities.
