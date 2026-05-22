# Mental Health Employee Clustering

## Project Overview

This project analyzes survey data from technology-oriented employees to support an HR pre-emptive mental health program.
Using unsupervised machine learning, the goal is to identify meaningful employee clusters and provide actionable insights
for targeted HR measures.

---

## Table of Contents

- [Use Case](#use-case)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [How it works](#how-it-works)
- [Usage](#usage)

---

## Use Case

The HR department of a technology-oriented company is launching a pre-emptive program to mitigate mental health issues
among its staff.
As a data scientist, the task is to:

- Explore and preprocess a high-dimensional survey dataset
- Reduce dimensionality while preserving the main characteristics of the data
- Identify employee clusters based on their survey responses
- Provide visualizations and insights to support targeted HR measures

---

## Dataset

This project uses a mental health survey dataset from technology-oriented employees.
The dataset contains 1,433 participants and 63 features covering topics such as mental health disorders,
workplace openness, employer support and treatment-seeking behavior.

The dataset is not included in this repository due to licensing.
It can be downloaded from [Kaggle](https://www.kaggle.com/datasets/osmi/mental-health-in-tech-survey).

---

## Project Structure

```
Case_Study_ML/
├── data/
│   └── raw/
│       └── mental_health_data.csv     # Raw survey dataset
├── notebooks/
│   └── analysis.ipynb                 # Main analysis notebook
├── outputs/
│   └── *.png                          # Generated visualizations
├── requirements.txt                   # Minimal Python dependencies
├── full_requirements.txt              # Full environment dependencies
└── README.md                          # Project documentation
```

---

## Installation

### 1. Clone the repository

```
git clone https://github.com/fessedini/unsupervised_learning.git
cd unsupervised_learning
```

### 2. Create and activate a virtual environment

```
python3.9 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```
pip install -r requirements.txt
```

This will install all required packages, including:

- **pandas and numpy** – for data manipulation and analysis
- **matplotlib and seaborn** – for visualizations
- **scikit-learn** – for PCA and K-Means clustering
- **missingno** – for missing value visualization

---

## How it works

### Analysis Pipeline

The analysis follows a structured pipeline:

1. **Exploratory Data Analysis (EDA)** – Initial inspection of the dataset, missing value analysis and key distribution
visualizations
2. **Preprocessing** – Encoding of categorical variables, outlier treatment, standardization and imputation of missing 
values
3. **Dimensionality Reduction** – PCA to reduce 51 features to 22 principal components retaining 81.2% of variance
4. **Clustering** – K-Means clustering with k=4, determined using the Elbow Method and Silhouette Score

### Identified Clusters

| Cluster | Name | n |
|---------|------|---|
| 0 | Unaffected | 399 |
| 1 | Affected with High Trust | 268 |
| 2 | Affected with Low Trust | 348 |
| 3 | No Prior Experience | 131 |

---

## Usage

Open the Jupyter Notebook and run all cells:

```
jupyter notebook analysis.ipynb
```