# Diabetes Prediction Project

## Objective

The goal of this project is to analyze clinical data and build a machine learning model to predict the likelihood of diabetes in patients.

This project simulates a real-world data workflow combining SQL, Python, data analysis, and machine learning.

---

## Workflow

1. Load data from CSV
2. Store data in a SQL database (SQLite)
3. Perform data extraction and filtering using SQL
4. Conduct exploratory data analysis (EDA) using Pandas and Matplotlib
5. Prepare data for machine learning
6. Train and evaluate classification models

---

## Data Source

The dataset used in this project is publicly available on Kaggle:

 https://www.kaggle.com/datasets/ziya07/diabetes-clinical-dataset100k-rows

Due to file size limitations, the dataset is not included in this repository.
Please download it manually and place it in the project root folder as:

```
diabetes_dataset_with_notes.csv
```

---

## Data Cleaning (SQL)

Instead of modifying the original database, data cleaning is performed dynamically using SQL filters:

* Remove unrealistic ages (age < 10)
* Remove extreme BMI values (BMI > 60)
* Exclude missing glucose values

This approach simulates real-world database querying practices.

---

## Exploratory Data Analysis

Key insights:

* Age distribution shows higher concentration in older populations
* BMI distribution centers around overweight ranges (~28)
* Blood glucose levels are right-skewed with higher values linked to diabetes
* HbA1c and glucose levels show strong correlation with diabetes

---

## Machine Learning

### Models Used

* Logistic Regression (baseline model)
* Random Forest (advanced model)

### Key Results

**Logistic Regression**

* High recall for diabetes detection (0.87)
* Better at identifying positive cases
* More false positives (acceptable in medical context)

**Random Forest**

* Higher overall accuracy (0.97)
* Higher precision
* Lower recall for diabetes (0.69)

---

## Conclusion

Although Random Forest achieved higher accuracy, Logistic Regression was selected as the preferred model due to its higher recall.

In healthcare scenarios, minimizing false negatives is critical, making recall more important than accuracy.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* SQLite

---

## How to Run

1. Clone the repository
2. Download the dataset from Kaggle
3. Place the CSV file in the project folder
4. Install dependencies:

```
pip install -r requirements.txt
```

5. Open and run the Jupyter Notebook:

```
jupyter notebook
```

---

## Project Structure

```
├── diabetes_prediction.ipynb
├── requirements.txt
└── README.md
```

---

## Notes

This project is designed as a portfolio project to demonstrate:

* SQL + Python integration
* Data cleaning and preprocessing
* Exploratory data analysis
* Machine learning fundamentals
* Model evaluation and comparison

---
