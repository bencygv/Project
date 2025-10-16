# [CAR SALES & PRICING ANALYSIS PROJECT] 🚀

This project analyzes a car sales dataset to identify key drivers of car prices, sales performance, and resale value.

It also explores design–efficiency trade-offs, vehicle segmentation, and builds a price predictive model based on car specifications.

## 📊 Project Overview

**Problem Statement:** 

Understand how different car features — such as engine size, horsepower, vehicle type, and design dimensions — influence market outcomes: price, sales, and resale value.

**Goal:** 

Uncover market insights, evaluate design–efficiency trade-offs, define vehicle tiers, and develop regression models to predict price.

- 1. Car Pricing & Influencing Factors

    * Quantify which features most influence price (horsepower, engine size, dimensions, Power_perf_factor).
    * Explore how performance and design contribute to pricing tiers.
    * Analyze correlations between price, resale value, and performance.

- 2. Sales & Market Trends

    * Identify high-performing manufacturers and vehicle types.
    * Analyze how changes in price affect car sales volumes to understand price sensitivity and demand behavior.
    * Explore the impact of fuel efficiency and performance on demand.

- 3. Resale Value

    * Rank manufacturers and models by value retention.
    * Examine how vehicle type and performance affect depreciation.

- 4. Design & Efficiency Trade-offs
    * Assess relationships between engine size, curb weight, and fuel efficiency.
    * Evaluate power-to-weight and economy trade-offs.

- 5. Vehicle Segmentation
    * Categorize vehicles into Economy, Mid-Range, Premium, and Luxury tiers using quantile segmentation.
    * Compare average performance, design, and financial indicators by segment.

- 6. Predictive Modeling
    * Build regression models to predict price using linear regression.
    * Evaluate model accuracy and identify the most influential predictors.

**Methods:** 

    A combination of Exploratory Data Analysis (EDA), correlation and regression analysis, feature engineering, and predictive modeling techniques were used.
    The workflow included:

    * Data Cleaning & Preprocessing – handling missing values, encoding categorical variables, and creating derived features (e.g., Power_to_Weight, Depreciation_Percentage).

    * Exploratory Data Analysis (EDA) – visualizing distributions, relationships, and manufacturer-level summaries.

    * Correlation & Elasticity Studies – measuring relationships between price, sales, and performance metrics.

    * Segmentation Analysis – identifying natural vehicle groupings based on performance and design attributes using qcut method.

    * Predictive Modeling – applying linear regression to estimate Price_in_thousands and evaluating performance using R², MAE, and RMSE.

## 🎯 Key Findings

- Pricing Drivers
    * Power_to_Weight is positively associated with price; core performance metrics (Engine_size, Horsepower) are the strongest price drivers, with design attributes contributing secondary effects.
    * Engine size, horsepower, and power-to-weight ratio are the strongest predictors of price.

- Sales Behavior
    * Sales show mild price sensitivity; higher Fuel_efficiency tends to correlate with better sales, reflecting value-conscious demand.
    * Performance alone does not guarantee higher sales.
    * Mid-range, fuel-efficient vehicles achieve the highest sales volumes.

- Resale & Depreciation
    * Performance-heavy cars depreciate faster; efficiency positively associates with resale value.
    * Depreciation averages 35–45% of the original price after 1 year.
    * Luxury and premium vehicles tend to retain value better; performance cars depreciate faster.
    * Toyota and BMW exhibit the highest average resale ratios among manufacturers.

- Design–Efficiency Trade-offs
    * Fuel efficiency declines with increasing horsepower and engine size, indicating a power–economy trade-off.
    * Compact and economy vehicles are the most efficient; performance SUVs show lower mileage.
    * Higher curb weight and engine size increase performance but reduce fuel efficiency.

- Temporal & Launch Trends
    * Newer model launches show higher average prices and improved fuel efficiency.
    * Depreciation has stabilized over time, suggesting better engineering and stronger brand positioning.

- Segmentation Insights
    * Quantile-based segmentation reveals four tiers—from Economy to Luxury—each distinct in pricing, performance, and depreciation.
    * Luxury cars have the highest horsepower and lowest efficiency; economy cars lead in fuel performance and sales volume.

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

pandas • numpy • matplotlib • seaborn • scikit-learn • missingno

**Tools:**

Jupyter Notebook • Git • GitHub

## 📊 Data

**Data Source:** 

[Kaggle – Car Sales Dataset](https://www.kaggle.com/datasets/gagandeep16/car-sales/data)

**Dataset Size:** 
157 rows × 16 columns, 16.02 kB

**Key Features:** 

    * Price_in_thousands – List price (in thousands).
    * Sales_in_thousands – Units sold (in thousands).
    * Year_resale_value – Average resale value after 1 year.
    * Manufacturer, Model, Vehicle_type – Categorical attributes.
    * Horsepower, Engine_size – Core performance indicators.
    * Fuel_efficiency, Fuel_capacity – Efficiency metrics.
    * Curb_weight, Wheelbase, Length, Width – Design characteristics.
    * Power_perf_factor – Composite performance metric.
    * Latest_Launch – Most recent launch date (datetime).

## 🤖 Methodology

### **1. Data Preprocessing**

    * Checked for duplicates (none found).  
    * Renamed `__year_resale_value` → `Year_resale_value`. 
    * Converted columns: Manufacturer, Model, Vehicle_type → categorical; Latest_Launch → datetime
    * Kept only rows with ≤ 2 missing values. 
    * Filled missing values:
        - `Price_in_thousands`, `Power_perf_factor` → median imputation.  
        - `Curb_weight`, `Fuel_efficiency`, `Year_resale_value` → regression-based imputation.
    * Created derived metrics: 
        - `Depreciation_Percentage` and `Retention_Ratio`.  
        - `Power_to_Weight` and `Launch_Year` from Latest_Launch

### **2. Correlation Analysis**

    * Assessed correlations between numeric features and outcomes.
    
### **3. Exploratory Data Analysis (EDA)**

    * Visualized distributions and missingness patterns.
    * Generated price, sales, and efficiency comparisons by manufacturer and vehicle type.

#### 🔹 Price Analysis

        - Manufacturer-level price summaries, price distribution by Vehicle_type, Top-N most expensive models. 
        - Relationships with design/performance features (Engine_size, Horsepower, Curb_weight, Power_to_Weight).

#### 🔹 Sales Analysis

        - Total and average Sales by Manufacturer and Vehicle_type; Top-N best-selling models. 
        - Price vs Sales sensitivity checks; associations with Fuel_efficiency and Power_perf_factor.

#### 🔹 Resale & Depreciation

        - Depreciation_Percentage and Retention_Ratio profiles by Manufacturer and Vehicle_type.
        - Associations with performance/design features and Fuel_efficiency.

#### 🔹 Design & Efficiency

        - Relationships of Curb_weight, Width, Engine_size with Fuel_efficiency.
        - Performance-efficiency trade-offs (Horsepower vs mileage).

#### 🔹 Temporal & Launch Trends

        - Compared car models to see how launch year affects sales and value. 

### **4. Vehicle Segmentation**

    * Cars segmented via price quartiles (pd.qcut) into:
        - Economy • Mid-Range • Premium • Luxury
    * Compared average sales, performance, design, and financial indicators across tiers.
    * Visualized relationships (Price vs. Depreciation, Horsepower vs. Fuel Efficiency) by segment.

### **5. Predictive Modeling**

#### 🔹 Price Prediction Model
        - Predict `Price_in_thousands` from design & performance features using Linear Regression.  

### Modeling Approach  

**Price Prediction Model** — predicts `Price_in_thousands` using performance and design features.

    The model was trained using an **80/20 train-test split**, and missing values were imputed using regression-based techniques before modeling.

### Evaluation

    * Model performance was evaluated using three main metrics: 
        - **R² Score** — indicates how well model features explain the variation in the target variable. 
        - **MAE (Mean Absolute Error)** — measures average prediction error.  
        - **RMSE (Root Mean Squared Error)** — penalizes larger errors more strongly.

    * Visual checks were performed using **actual vs predicted plots** and to verify linearity.
     
## 📈 Results

**Model Performance:**

    * Price Prediction (Linear Regression) using `Power_perf_factor` and `Horsepowe`.
        - R² Score: 0.963
        - MAE: 2.34 (in thousands)
        - RMSE: 3.77 (in thousands)

**Key Visualizations:**

    * Correlation Heatmap of All Numeric Features
    * Price vs Horsepower / Engine Size (with regression fit)
    * Power-to-Weight vs Price and vs Fuel Efficiency
    * Price Distribution by Manufacturer and Vehicle Type
    * Top 10 Best-Selling and Most Expensive Models
    * Average Resale Value and Depreciation by Manufacturer
    * Top 10 Most Fuel-Efficient Models
    * Launch Year vs Price / Efficiency / Depreciation
    * Quantile-Based Vehicle Segmentation (barplots and scatterplots)

## 🚀 Reproducibility

### Setup
```bash
# Clone Repository
git clone [https://github.com/bencygv/Project.git]
cd [Project]

# Install Dependencies
uv sync
```

### Execution
```bash
# Run Notebooks in this order:
# 1. notebooks/01_exploration.ipynb
```

## 🎓 About this Project

**Context:** 
Context: Data Analysis Portfolio Project [StackFuel]

**Timeframe:** 
3 Weeks

**Author:** 
Bency George Varghese

## 📞 Contact

**GitHub:** [@bencygv](https://github.com/bencygv)  
**E-Mail:** bencygv@gmail.com  
**LinkedIn:** [Your Profil](https://linkedin.com/in/
your-profil)

## 🙏 AcknowledgementsDataset: 

    * Kaggle (by gagandeep16)
    * Open-source libraries (pandas, scikit-learn, seaborn)
    * Community support and StackFuel mentors

---

**⭐ If you like this project, consider giving it a star!**
