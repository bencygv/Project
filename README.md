# [CAR SALES & PRICING ANALYSIS PROJECT] 🚀

This project analyzes a car sales dataset to identify key drivers of car prices, sales, and resale value. Extending the study by exploring design-efficiency trade-offs, and vehicle segmentation. The analysis also includes a predictive modelling to estimate car prices based on vehicle specification.

## 📊 Project Overview

**Problem Statement:** 
Understanding how different car features (engine size, horsepower, vehicle type, etc.) influence market outcomes: sales, pricing, and long-term resale value.

**Goal:** 
To uncover strategic market insights, analyze vehicle design trade-offs, and build a predictive model to estimate car prices. 

1. Car Pricing & Influencing Factors
    * What factors influence car price most strongly?
    * How does horsepower relate to price?
    * Is Power_perf_factor correlated with resale value or sales?
    * Do larger / more powerful cars sell better than smaller ones?

2. Sales & Market Trends
    * Which manufacturers dominate sales volume?
    * How do sales and prices trend over time with new launches?
    * What is the relationship between Price_in_thousands and Sales_in_thousands?
    * Any pattern of sales linked to launch year/month?

3. Resale Value
    * Which manufacturers retain value best?
    * Does vehicle type affect depreciation?
    * Which manufacturers have the highest average resale values?

4. Design & Efficiency Trade-offs
    * How do price and fuel efficiency relate by manufacturer?
    * Influence of design factors (Wheelbase, Width, Length, Curb_weight) on fuel efficiency.
    * Trade-off between Engine_size and Fuel_efficiency.

5. Vehicle Segmentation
    * What is the distribution of vehicle types?
    * Can we cluster vehicles into natural groups (economy, family, performance, luxury)?

6. Predictive Modeling
    * Can we build a predictive model to estimate a car’s price from its features?

**Methods:** 
<!-- Exploratory Data Analysis (EDA), correlation analysis, and regression modeling. -->

## 🎯 Key Findings

<!-- Your main insights in 3–5 bullet points -->
- 📈 **Finding 1:** Short description
- 🔍 **Finding 2:** Short description  
- 💡 **Finding 3:** Short description

## 📁 Repository Structure

```
├── data/
│   ├── raw/                    # Original data
│   └── processed/              # Cleaned Data
├── notebooks/                  # Jupyter Notebooks
│   └── 01_exploration.ipynb    # Data exploration
├── src/dpp                     # Python Modules
├── test/                       # Unit Tests
├── pyproject.toml              # Project configuration
└── docs/                       # Additional Documentation
```

## 🔧 Technologies Used

**Programming Languages:**
Python

**Libraries & Frameworks:**
pandas, scikit-learn, matplotlib, numpy, seaborn

**Tools:**
Jupyter, Git, GitHub

## 📊 Data

**Data Source:** 
Kaggle - Car Sales Dataset (https://www.kaggle.com/datasets/gagandeep16/car-sales/data)

**Dataset Size:** 
157 rows × 16 columns, 16.02 kB

**Key Features:** 
    * Price_in_thousands: The vehicle's list price (in thousands).
    * Sales_in_thousands: The volume of vehicles sold by model (in thousands).
    * __year_resale_value: The estimated resale value of the car (in thousands).
    * Manufacturer / Model / Vehicle_type: The manufacturer, model and the type of car.
    * Horsepower / Engine_size: Key performance metrics influencing price and design.
    * Fuel_efficiency / Fuel_capacity
    * Curb_weight / Wheelbase / Length / Width: Physical design factors
    * Latest_Launch: The date the model was most recently launched.
    * Power_perf_factor: Power Performance Factor.

## 🤖 Methodology

### Data Preprocessing
    1. Checked for duplicate values and found that there was none.
    2. Renamed __year_resale_value column to Year_resale_value.
    3. Converted object columns to categorical type.
    4. Converted Latest_Launch object datatype to datetime.
    5. Kept only rows that have fewer than 3 missing values.
    
    . Replaced NaN values of various columns using MEDIAN or LINEAR REGRESSION

### Modeling Approach  
<!-- Which models did you test? -->

### Evaluation
<!-- How did you evaluate the results? -->

## 📈 Results

**Model Performance:**
<!-- Your best metrics (Accuracy, RMSE, etc.) -->

**Key Visualizations:**
<!-- Reference key plots in your notebooks -->

## 🚀 Reproducibility

### Setup
```bash
# Clone Repository
git clone [YOUR-REPO-LINK]
cd [REPO-NAME]

# Install Dependencies
uv sync
```

### Execution
```bash
# Run Notebooks in this order:
# 1. notebooks/01_exploration.ipynb
# 2. notebooks/02_preprocessing.ipynb  
# 3. notebooks/03_modeling.ipynb
# 4. notebooks/04_results.ipynb
```

## 🎓 About this Project

**Context:** 
<!-- As part of Data Analysis Portfolio Project with StackFuel. -->

**Timeframe:** 
<!-- When did you complete the project? -->

**Author:** 
Bency George Varghese

## 📞 Contact

**GitHub:** [@bencygv](https://github.com/bencygv)  
**E-Mail:** bencygv@gmail.com  
**LinkedIn:** [Your Profil](https://linkedin.com/in/
your-profil)

## 🙏 Acknowledgements

<!-- Mention people or resources that helped you -->

---

**⭐ If you like this project, consider giving it a star!**
