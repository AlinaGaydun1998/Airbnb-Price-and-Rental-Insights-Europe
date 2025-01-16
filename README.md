# European Airbnb Price Determinants and Key Metrics

This project analyzes **Airbnb rental data** for major European cities, including **Amsterdam, Rome, Paris, Vienna, Budapest, Berlin, London, and Lisbon**. The goal of this analysis is to uncover key factors influencing rental prices and guest satisfaction, as well as provide actionable insights for travelers, hosts, and property investors.

## Dataset Overview
The dataset used in this project provides Airbnb rental information, including:
- **Listing price** (`realSum`)
- **Room type** (`room_type`)
- **Host status** (`host_is_superhost`)
- **Amenities** (`biz`)
- **Location details** (latitude, longitude, proximity to city center, metro, and attractions)

The data source is from [Kaggle](https://www.kaggle.com/datasets/thedevastator/airbnb-price-determinants-in-europe/data).

## Dataset Overview

The dataset contains Airbnb rental information for major European cities, including Amsterdam, Rome, Paris, and more. Below is a brief description of the key columns:

| **Column Name**           | **Description**                                                                 |
|---------------------------|---------------------------------------------------------------------------------|
| `realSum`                 | The total price of the Airbnb listing.                                           |
| `room_type`               | The type of room offered (e.g., private room, shared room, entire home/apt).     |
| `person_capacity`         | The maximum number of people that can be accommodated in a listing.              |
| `host_is_superhost`       | Whether the host is a superhost (1) or not (0).                                 |
| `cleanliness_rating`      | The rating for cleanliness based on guest reviews.                              |
| `guest_satisfaction_overall` | The overall guest satisfaction rating.                                         |
| `bedrooms`                | The number of bedrooms in the listing.                                          |
| `dist`                    | Distance from the city center.                                                  |
| `metro_dist`              | Distance from the nearest metro station.                                        |
| `lat` and `lng`           | Latitude and longitude of each listing.                                         |
| `attr_index_norm`         | Normalized version of the attraction index, scaled between 0 and 100.           |

For a more detailed analysis of these columns, please refer to the Jupyter notebook.

### Data Format:
- **CSV format**: The dataset is provided in CSV format, making it easy to load and process using data manipulation libraries such as **Pandas**.
- **Numerical columns**: Many of the columns (such as `realSum`, `cleanliness_rating`, `dist`, `metro_dist`) are continuous numerical variables.
- **Categorical columns**: Columns such as `room_type`, `host_is_superhost` contain categorical data.
- **Geographical data**: The dataset includes latitude (`lat`) and longitude (`lng`) for each listing, which can be used for geospatial analysis or mapping.

## Analytical Methods and Tools Used
This project leverages various **data analysis** methods to answer key questions related to Airbnb pricing and guest satisfaction:

### Tools:
- **Python Libraries**:
  - `numpy`, `pandas`: Data manipulation and analysis.
  - `matplotlib`, `seaborn`: Data visualization.
  - `scipy`: Statistical tests (e.g., Shapiro-Wilk test, chi-square test).
  - `sklearn`: Machine learning (e.g., Random Forest, Linear Regression, KMeans clustering).
  - `statsmodels`: Statistical models and analysis.

### Key Questions Explored:
1. **Feature Importance**: Using **Random Forest** to identify key factors affecting rental prices (`realSum`).
2. **Correlation Analysis**: Exploring relationships between the most influential variables and how they correlate with each other.
3. **Rental Price Differences**: Are there significant differences in rental prices between weekdays and weekends across cities?
4. **Superhost Effect**: Does being a **Superhost** affect the type of accommodation offered and the pricing?
5. **Room Type Preferences**: Investigating the frequency of room type selection by guests.
6. **Geographical Impact on Room Type**: How do proximity factors (city center, metro, attractions) influence the choice of room type?
7. **City Cleanliness & Guest Satisfaction**: Ranking cities based on cleanliness ratings and overall guest satisfaction.
8. **Bedroom and Capacity Impact**: Investigating how the number of bedrooms and guest capacity influence rental prices.
9. **Geographical Factors on Price**: Analyzing how distance and location-related factors (latitude, longitude, proximity to attractions/restaurants) impact rental prices.
10. **Geography and Guest Satisfaction**: How do geographical factors like latitude, longitude, and distance affect guest satisfaction?

## Tableau Dashboard
A **Tableau dashboard** was created to visually explore and present the findings. It includes key metrics and insights, including:
- Average rental prices by city and room type.
- Impact of superhost status on rental prices.
- Frequency of room type selection and its geographical impact.
- Geographic heat maps showing rental price density, longitude and latitude clustering, and which proximity categories to restaurants and metro each property falls into.

You can view the Tableau dashboard [here](https://public.tableau.com/shared/JFK2JC9WY?:display_count=n&:origin=viz_share_link).

