# [CAR SALES DATA ANALYSIS PROJECT] 🚀

This project analyzes a car sales dataset to explore pricing, sales trends, resale values, efficiency trade-offs, and vehicle segmentation. The analysis also includes a predictive modelling to estimate car prices based on vehicle specification.

## 📊 Project Overview

**Problem Statement:** 
Understanding how different car features (engine size, horsepower, vehicle type, etc.) influence sales, pricing, and resale value.

**Goal:** 
To uncover insights into market trends, vehicle design trade-offs, and build a predictive model to estimate car prices. 
1. Car Pricing & Influencing Factors
    * What factors influence car price most strongly?
    * How does horsepower relate to price?
    * Is Power_perf_factor correlated with resale value or sales?
    * Do larger / more powerful cars sell better than smaller ones?

2. Sales & Market Trends
    * Which manufacturers dominate sales volume?
    * How do sales and prices trend over time with new launches (Latest_Launch)?
    * What is the relationship between Price_in_thousands and Sales_in_thousands?
    * Any pattern of sales linked to Latest_Launch year/month?

3. Resale Value
    * Which manufacturers/models retain value best (One_Year_Resale_Value vs Price_in_thousands)?
    * Does vehicle type (Passenger vs Car) affect depreciation?
    * Which manufacturers have the highest average resale values?

4. Design & Efficiency Trade-offs
    * How do price and fuel efficiency relate by make or model?
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
<!-- Python-->

**Libraries & Frameworks:**
<!-- pandas, scikit-learn, matplotlib, numpy, seaborn -->

**Tools:**
<!-- Jupyter, Git, etc. -->

## 📊 Data

**Data Source:** 
Kaggle - Car Sales Dataset (https://www.kaggle.com/datasets/gagandeep16/car-sales/data)

**Dataset Size:** 
157 rows × 16 columns, 16.02 kB

**Key Features:** 
<!-- * Sales_in_thousands: Sales volume per model
     * _year_resale_value: Resale value after one year 
     * Price_in_thousands: Vehicle price 
     * Engine_size, Horsepower, Fuel_capacity, Fuel_efficiency 
     * Wheelbase, Width, Length, Curb_weight
     * Manufacturer, Model, Latest_Launch, Power_perf_factor -->

## 🤖 Methodology

### Data Preprocessing
<!-- 1. Check for duplicate values and found that there was no duplicate values.
     2. Replaced NaN values of various columns using MEDIAN or LINEAR REGRESSION -->

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
