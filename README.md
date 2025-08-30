# Delhivery-Feature-Engineering 🚚📦
This repository contains **data analysis and feature engineering** performed on the Delhivery dataset.   The goal is to preprocess raw logistics data, apply feature transformations, and extract insights that can be used for downstream **machine learning models** and **business decision-making**.

## 📌 Project Overview
  Objective: Analyze Delhivery's shipment data to uncover operational patterns, identify outliers, and build engineered features to support advanced predictive modeling.

  Dataset: Contains over 144,000 records encompassing trip details, route info, time, distance, center names, and segment-level breakdowns.

## Key Steps & Methodologies
  1. Data Cleaning & Exploration
     Handled missing values (only ~0.38% missing; dropped for simplicity and reliability).

     Inspected datatypes, unique values, & summary statistics.

     Aggregated trip segments to form a consolidated trip-level dataset.

  2. Feature Engineering
    Extracted granular details from center names and locations (city, place, code, state).
    
    Derived rich time features: trip creation year/month/day/week/hour.
    
    Computed trip-level metrics (total trip time, segmented times/distances).
    
    Performed one-hot encoding for categorical variables (route type, data tag).

  3. Outlier Detection & Handling
    Used boxplots and descriptive statistics to visualize and identify outliers in all major numeric columns (times, distances).
    
    Applied the IQR method to remove extreme values, reducing the dataset to 8,134 entries, ensuring robust downstream analyses.

  4. Hypothesis Testing & Statistical Analysis
    Compared trip totals vs. scan times, actual vs. estimated/OSRM metrics using nonparametric tests (Wilcoxon).
    
    Checked normality (Shapiro-Wilk, QQ plots), variance homogeneity (Levene's test).
    
    Found statistically significant differences between actual and estimated values—highlighting real-world delivery deviations.

  5. Data Normalization
    Standardized numerical features using StandardScaler for improved machine learning model compatibility.

  6. Visualization & Insights
    Generated pie charts, boxplots, barplots, scatterplots, QQ plots, and KDEs to understand distributions and patterns.
    
    Mapped busiest corridors, peak hours/days, and top cities & states for both source and destination.

## 📊 Major Findings
- FTL route type is dominant (68.8%).

- Peak trip creation hours are at night; September is busiest month.

- Top source & destinations: Haryana and Karnataka are crucial operational hubs.

- Statistically significant differences exist between actual and estimated (OSRM) times and distances.

- Most numeric variables exhibit significant outliers, which were handled for modeling.

- High delivery counts cluster around specific corridors and places, guiding resource allocation.

## 💡 Business Recommendations
- Improve route planning: Integrate real-time traffic and predictive delays.

- Optimize hub operations: Automation, peak-hour staffing.

- Focus on delay-prone routes: Review contracts, explore alternate logistics.

- Redesign SLAs: Align with observed ground realities.

- Prioritize high-deviation trips: Real-time monitoring dashboards.

- Leverage feature engineering: Build models to flag risky trips.

- Standardize processes: SOP enforcement, staff training for outlier-heavy centers.


🛠️ Tech Stack

- Python: Pandas, NumPy, Scikit-learn

- Visualization: Matplotlib, Seaborn

- Jupyter Notebook


---

## ⚙️ Installation
Clone the repository:
```bash
git clone https://github.com/your-username/delhivery-feature-engineering.git
cd delhivery-feature-engineering
```

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange)
![License](https://img.shields.io/badge/License-MIT-green)
