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

This section focuses on creating new features and preparing the data for modeling.

1.  **Time-based Features:**
    *   The 'timestamp' column is converted to a datetime object.
    *   New columns 'hour', 'weekday', and 'month' are extracted from the 'timestamp'.

2.  **Label Encoding:**
    *   The categorical 'primary_use' column is converted into numerical format using Label Encoding.

3.  **Handling Missing Values:**
    *   Missing values in the 'meter_reading' column are imputed with the median value of the column.

4.  **Defining Target and Features:**
    *   The target variable is identified as 'anomaly'.
    *   A list of features to be used for modeling is defined, including both original and newly created features.

5.  **Splitting Data:**
    *   The dataset is split into feature matrix (`X`) and target vector (`y`).

6.  **Scaling Features:**
    *   Numerical features in `X` are scaled using `StandardScaler` to ensure they are on a similar scale, which is important for many machine learning algorithms.

7.  **Train-Test Split:**
    *   The scaled data is split into training and testing sets (`X_train`, `X_test`, `y_train`, `y_test`) for model training and evaluation. The split is stratified based on the target variable to maintain the proportion of classes in both sets. A `random_state` is used for reproducibility.
