# Iris Flower Dataset — Exploratory Data Analysis (EDA)

## Project Overview

This project explores the Iris flower dataset using Python to understand the differences between three Iris species: Setosa, Versicolor, and Virginica.

The analysis focuses on understanding the dataset, checking data quality, comparing numerical measurements, exploring relationships between variables, and identifying potential outliers through visualizations.

This is a beginner-level Exploratory Data Analysis (EDA) project completed as part of my ongoing practice in Data Analytics.

## Objectives

- Understand the structure and characteristics of the dataset.
- Inspect numerical and categorical variables.
- Identify missing values and duplicate records.
- Compare average flower measurements across species.
- Investigate relationships between petal length and petal width.
- Visualize distributions and identify potential outliers.
- Practise interpreting data and communicating analytical findings.

## Dataset Description

The Iris dataset contains measurements of flowers belonging to three species.

**Dataset source:** Seaborn's built-in Iris dataset, loaded using `sns.load_dataset("iris")`.

The original dataset contains 150 observations and 5 columns.

| Column | Description | Data type |
|---|---|---|
| `sepal_length` | Length of the sepal | Numerical |
| `sepal_width` | Width of the sepal | Numerical |
| `petal_length` | Length of the petal | Numerical |
| `petal_width` | Width of the petal | Numerical |
| `species` | Iris flower species | Categorical |

The three species are Setosa, Versicolor, and Virginica.

## Tools and Technologies

- **Python** — Programming language used for analysis.
- **Pandas** — Data inspection, cleaning, grouping, and aggregation.
- **NumPy** — Numerical computing support.
- **Matplotlib** — Data visualization.
- **Seaborn** — Statistical visualization and dataset loading.
- **Google Colab** — Notebook environment used for analysis.
- **GitHub** — Project versioning and portfolio documentation.

## Project Workflow

### 1. Data Loading and Inspection

The dataset was loaded into a Pandas DataFrame.

Initial inspection included:

- Viewing the first few rows.
- Checking the number of rows and columns.
- Inspecting column names and data types.
- Generating descriptive statistics using `df.describe()`.

The original dataset contained 150 rows and 5 columns.

### 2. Data Quality Assessment

Missing values, duplicate records, and data types were checked.

**Missing values:** No missing values were detected.

**Duplicate records:** One duplicate row was identified. A separate cleaned DataFrame was created using `drop_duplicates()`, reducing the number of rows from 150 to 149. The original DataFrame was preserved.

**Data types:** The four measurement columns were stored as `float64`, while the species column was stored as `object`. These data types were appropriate for the analysis.

The duplicate was removed for this exercise. In real-world analyses, duplicate records should be investigated before removal because identical measurements do not necessarily indicate erroneous records.

### 3. Group-wise Statistical Analysis

The mean of each numerical measurement was calculated for every species using Pandas `groupby()` and `mean()`.

This analysis helped compare sepal and petal measurements across the three species.

The mean petal lengths were approximately:

| Species | Mean petal length |
|---|---:|
| Setosa | 1.462 |
| Versicolor | 4.260 |
| Virginica | 5.561 |

These results show substantial differences in average petal length across the species.

### 4. Data Visualization

Several visualizations were created to explore the dataset.

#### Bar Chart — Mean Petal Length by Species

The bar chart compared the average petal length of each species.

**Observation:** Virginica had the highest average petal length, while Setosa had the lowest. Versicolor fell between the two.

#### Scatter Plot — Petal Length vs. Petal Width

A scatter plot was used to investigate the relationship between petal length and petal width.

**Observation:** The plot showed a strong positive relationship: flowers with longer petals generally tended to have wider petals.

The Pearson correlation coefficient was approximately **0.963**, indicating a very strong positive linear association across the combined observations.

#### Species-Coloured Scatter Plot

A second scatter plot used species as the colour variable to compare the groups.

**Observation:** Setosa was clearly separated from the other two species based on petal measurements. Versicolor and Virginica showed some overlap.

Colour-coding helped reveal the species clusters more clearly.

#### Box Plot — Petal Length Distribution by Species

A box plot was used to compare the medians, spreads, and potential outliers of petal length across the three species.

**Observations:**

- Virginica had the highest median petal length.
- Setosa had the lowest median petal length.
- Potential outliers were flagged for Setosa and Versicolor using the box plot's default rule.
- No observations were flagged as potential outliers for Virginica in this plot.

Potential outliers require further investigation and should not automatically be removed.

## Key Findings

1. **Petal length differs substantially across species.** Virginica had the highest mean petal length, followed by Versicolor and Setosa.

2. **Petal length and petal width have a very strong positive linear association.** The correlation coefficient was approximately 0.963 across the combined dataset.

3. **Setosa is clearly separated from the other species in petal measurements.** The species-coloured scatter plot revealed distinct clusters, with some overlap between Versicolor and Virginica.

4. **The distributions differ across species.** The box plot showed different median petal lengths and flagged potential outliers in Setosa and Versicolor.

5. **Data quality checks found no missing values and one duplicate row.** A cleaned DataFrame containing 149 rows was used for the subsequent analysis.

## Conclusion

This project provided practical experience in exploratory data analysis using Python. It covered data inspection, data quality checks, duplicate handling, group-wise aggregation, correlation analysis, and visualization.

The analysis revealed clear differences in petal measurements across the three Iris species and a strong positive association between petal length and petal width.

Through this exercise, I practised using Pandas for data analysis and Matplotlib and Seaborn for visualization, while developing my ability to interpret data and communicate findings.

## Skills Practised

- Exploratory Data Analysis (EDA)
- Data inspection and quality assessment
- Missing-value and duplicate checks
- Pandas grouping and aggregation
- Descriptive statistics
- Bivariate analysis
- Correlation analysis
- Data visualization
- Outlier identification
- Analytical interpretation

## Project Structure

```text
iris-flower-eda/
├── Iris_Flower_EDA.ipynb
└── README.md
```

## How to Run

1. Clone or download this repository.
2. Open `Iris_Flower_EDA.ipynb` in Google Colab or Jupyter Notebook.
3. Install the required libraries if they are not already available.
4. Run the notebook cells sequentially to reproduce the analysis.

The notebook loads the dataset directly through Seaborn, so a separate dataset file is not required.

## Future Improvements

- Explore the distributions of all four numerical measurements.
- Compare sepal measurements across species.
- Investigate correlations within individual species.
- Examine potential outliers in greater detail.
- Explore additional datasets and more advanced EDA techniques.

---

**Project Type:** Beginner Data Analytics / Exploratory Data Analysis

**Status:** Completed initial analysis

**Author:** Nazreen Shanavaz
