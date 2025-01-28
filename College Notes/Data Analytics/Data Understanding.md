
# Lecture 2: Data Exploration and Understanding

**Instructor:** Aurelia Power  
**Year:** 2024  
**Course:** H4030 Data Analytics  

---

## **Data Understanding Activities**
1. Collecting/Acquiring the data.
2. Describing/Exploring the data.
3. Initial survey and verification of data quality.
4. Reporting on findings.

---

## **What is a Dataset?**
- **Definition:** A collection of data, analogous to a database table.
- **Structure:**
  - **Rows:** Instances/examples/samples.
  - **Columns:** Attributes/features/variables.
- Example Dataset: Titanic dataset.

---

## **Steps in Data Understanding**
### 1. Collecting/Acquiring the Data
- Data must be organized into a single dataset for analysis.
- Sources include data warehouses, with considerations for:
  - Legal issues, departmental/political constraints, data format, connectivity, and timing.

### 2. Describing the Data
**Key Properties:**
- **Data Types:** Numerical or text/alphanumeric.
- **Dimensionality:** Number of attributes (columns).
- **Instances:** Number of rows.
  - Rule: At least 20× rows as columns for reliable pattern detection.
- **Distribution:** Check ranges of attribute values.
- **Resolution:** Scales of measurement (e.g., cm vs. m).

---

## **Types of Variables**
### Nominal
- Names without order (e.g., IDs, car registrations).
- Used in merging; usually discarded in modeling.

### Categorical
- Named groups without order (e.g., gender, eye color).
- Can be quantified by counting occurrences.

### Ordinal
- Ordered labels (e.g., {tall, medium, short}, grades).
- Cannot calculate meaningful distances between values.

### Interval
- Numerical values with intrinsic order (e.g., temperature).
- No true zero; ratios are not meaningful.

### Ratio
- Like interval but with a true zero (e.g., height, weight).
- Ratios and statistical calculations are valid.


**Comparison Table:**  

| Property                    | Nominal | Categorical | Ordinal | Interval | Ratio |
| --------------------------- | ------- | ----------- | ------- | -------- | ----- |
| Sequenced Scale Established | No      | No          | Yes     | Yes      | Yes   |
| Median                      | No      | No          | Yes     | Yes      | Yes   |
| Addition/Subtraction        | No      | No          | No      | Yes      | Yes   |
| Absolute Zero               | No      | No          | No      | No       | Yes   |


---

## **Data Quality Issues**
- **Bias:** Results not generalizable to the full population.
- **Noise:** Random error/variance in data.
- **Missing Data:** Missing attribute values (e.g., `NaN`).
- **Errors:** Incorrect values (e.g., negative age).
- **Outliers:** Unusual/unexpected values.
  - Identify via boxplots, scatter plots, or algorithms (e.g., LOF).
- **Pollution:** Misuse of fields or incorrect data placement.

---

## **Descriptive Statistics**
### Centrality Measures
- **Mean:** Average (sensitive to outliers).
- **Median:** Middle value (robust to outliers).
- **Mode:** Most frequent value.

### Dispersion Measures
- **Range:** Difference between max and min.
- **Standard Deviation:** Spread of values around the mean.

### Percentiles
- Indicate value thresholds for specific proportions (e.g., 25th, 50th, 75th percentiles).

---

## **Exploratory Data Analysis (EDA)**
### Key Steps
1. Understand attribute meanings.
2. Verify sufficient data (e.g., class balance).
3. Check quality issues.
4. Assess attribute utility for prediction.
5. Discover patterns.

### Examples:
- **Titanic Dataset:**
  - Attributes like `age`, `fare`, `sex`.
  - Class label: `survived` (Yes/No).

### Visualizations
- **Histograms:** Show frequency distributions.
- **Boxplots:** Highlight spread and outliers.
- **Scatter Plots:** Display relationships between numerical variables.
- **Grouped Bar Charts:** Compare class proportions for categorical variables.

---

## **Bivariate and Multivariate Analysis**
### Bivariate Analysis
- Compare one variable against the class label (e.g., fare vs. survived).
- Look for overlap in boxplots/density plots.

### Multivariate Analysis
- Combine multiple attributes to identify predictive patterns.
- Use colored scatter plots for visualization.

### Example:

```python
# Pandas for summary statistics
import pandas as pd

# Check missing values
missing_percentage = df.isnull().sum() / len(df) * 100
print(missing_percentage)

# Describe numerical attributes
print(df.describe())

# Correlation matrix
print(df.corr())
```

---

# Key EDA Question

1. Are there enough rows for reliable analysis?
2. Is the dataset balanced for each class?
3. Do attributes have predictive power?
4. Are there interesting relationships or patterns?


