`markdown
# Salary Data Analysis README

This README documents the analysis of a salary dataset using Pandas in Python. Below are the commands and operations performed on the dataset:

---

## File Import
python
import pandas as pd
data = pd.read_csv("Salary_Data.csv")


This command imports the salary data from a CSV file into a Pandas DataFrame.

---

## Displaying Data

python
data.head(5)
data.tail(10)
data.sample(7)


- `head(5)`: Displays the first 5 rows.
- `tail(10)`: Displays the last 10 rows.
- `sample(7)`: Displays 7 random rows.

---

## Descriptive Statistics

python
data.describe()
data.describe(include="all")


- Provides summary statistics for numerical and categorical columns.

---

## Data Visualization

python
data["Education Level"].value_counts().plot(kind="line")
data["Education Level"].value_counts().plot(kind="bar")
data["Education Level"].value_counts().plot(kind="barh")
data["Education Level"].value_counts().plot(kind="pie")
data["Education Level"].value_counts().plot(kind="hist")
data["Education Level"].value_counts().plot(kind="area")


Plots various visualizations to analyze the distribution of the "Education Level" column.

---

## Handling Missing Values

python
data.isnull().sum()
data.fillna(12, inplace=True)
data.dropna()


- `isnull().sum()`: Counts missing values in each column.
- `fillna(12)`: Replaces missing values with `12`.
- `dropna()`: Removes rows with missing values.

---

## Removing Duplicates

python
data.drop_duplicates()
data.duplicated()


- `drop_duplicates()`: Removes duplicate rows.
- `duplicated()`: Identifies duplicate rows.

---

## Data Access

python
data.loc[6703]
data["Job Title"]
data["Years of Experience"].info()
data["Salary"].sum()


- Accessing specific rows and columns.
- Summarizing column information.
- Calculating total salary.

---

## Output Example

### Sample Row Access

python
data.loc[6703]


**Output:**


Age                               26.0
Gender                          Female
Education Level            High School
Job Title              Sales Executive
Years of Experience                1.0
Salary                         35000.0
Name: 6703, dtype: object


---

## Memory Usage

python
data["Years of Experience"].info()


Displays memory usage and non-null count of the "Years of Experience" column.

---

## Salary Sum

python
data["Salary"].sum()


Calculates the total salary value in the dataset.

---

This file was created to document the commands used in analyzing the salary data, providing a comprehensive guide for replication and further analysis.


````
