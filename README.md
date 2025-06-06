# Anomaly-Detection-in-Power-Consumption-Time-Series-Using-Python

### Exploratory Data Analysis (EDA)

The exploratory data analysis phase involves understanding the dataset, identifying patterns, and visualizing relationships between features and the target variable. The following steps are performed:

- **Loading the data:** The `train_features.csv` file is loaded into a pandas DataFrame.
- **Inspecting the data:** Checking the first and last rows (`head()`, `tail()`), data types and non-null counts (`info()`), and summary statistics (`describe()`).
- **Handling missing values:** Identifying and assessing the extent of missing values (`isnull().sum()`).
- **Visualizations:** Generating plots to understand the distribution of key features and their relationships with `meter_reading`. This includes:
    - Distribution of `meter_reading` (Histogram).
    - `meter_reading` distribution by `primary_use` (Boxplot).
    - Hourly trend of `meter_reading` (Lineplot).
    - Correlation heatmap to see relationships between numerical features and `meter_reading`.
    - Distribution of `is_holiday` (Countplot).
    - Distribution of `square_feet` (Histogram).
    - Relationship between `air_temperature` and `meter_reading` (Scatterplot).
    - Distribution of `year_built` (Histogram).
    - `meter_reading` distribution by `site_id` (Violin plot).

These visualizations provide insights into the data distribution, potential outliers, and relationships that can be used for feature engineering and model selection.
