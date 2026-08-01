# 🏠 Airbnb NYC Data Analysis (EDA + Price Prediction)

## 📊 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on the **Airbnb NYC dataset** to understand pricing trends, room-type distribution, neighborhood patterns, and availability insights across New York City listings.

It's since been extended with a **price prediction model** — going beyond descriptive analysis into a supervised regression problem, testing how well listing price can actually be predicted from location, room type, and availability features.

This project demonstrates practical skills in:
- Data Cleaning
- Exploratory Data Analysis (EDA)
- Data Visualization
- Feature Engineering
- Regression Modeling
- Model Evaluation & Cross-Validation
- Insight Generation

---

## 🎯 Objectives

The main goals of this analysis:
- Analyze price distribution across different neighborhoods
- Compare room-type pricing trends
- Study availability of listings throughout the year
- Identify outliers and unusual listings
- Extract actionable business insights from data
- Test whether listing price can be predicted from available features, and understand where that prediction breaks down

---

## 📁 Dataset Information

Dataset contains information about:
- Listing Price
- Neighborhood Group
- Room Type
- Number of Reviews
- Availability (365 days)
- Host Listings Count
- Latitude & Longitude

Dataset size:
```
50,000+ Airbnb listings
```

---

## 🛠️ Tools & Technologies Used

Programming Language:
```
Python
```

Libraries:
```
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
```

Environment:
```
Jupyter Notebook
```

---

## 📂 Project Structure

```
eda-airbnb-nyc/
│
├── Air_bnb.ipynb                     # EDA notebook
├── Airbnb_Price_Prediction.ipynb     # Price prediction model (extension)
├── AB_NYC_2019(3).csv
└── README.md
```

---

## 🔍 Analysis Performed

### 1️⃣ Data Cleaning
- Checked missing values
- Removed unnecessary columns
- Verified data types
- Handled outliers

---

### 2️⃣ Univariate Analysis
Analyzed:
- Price distribution
- Room type frequency
- Neighborhood listing counts

---

### 3️⃣ Bivariate Analysis
Compared:
- Price vs Room Type
- Price vs Neighborhood Group
- Availability vs Listing Count

---

### 4️⃣ Data Visualization
Visualizations created:
```
Histograms
Boxplots
Bar Charts
Scatter Plots
Correlation Heatmap
```

---

## 📈 Key Insights (EDA)

Important observations from the dataset:
- Manhattan listings have the highest average prices
- Entire homes/apartments are more expensive than private rooms
- Some listings show extreme price outliers
- Availability varies significantly across neighborhoods
- Review distribution is uneven across listings

---

## 🤖 Price Prediction (Extension)

Beyond the EDA above, `Airbnb_Price_Prediction.ipynb` extends the analysis into a supervised
regression problem: predicting listing price from location, room type, and availability.

### Approach
- Engineered a **distance-from-city-center** feature from latitude/longitude, since raw coordinates don't mean much to a model on their own
- **Log-transformed** price and other skewed numeric features before training, since price is heavily right-skewed
- Compared **Linear Regression, Random Forest, and Gradient Boosting**
- Validated with **3-fold cross-validation**, not just a single train/test split
- Diagnosed model behavior with actual-vs-predicted and residual plots, not just a single accuracy number

### Results

| Model | Test MAE | Test R² |
|---|---|---|
| Linear Regression | $49.68 | 0.328 |
| Random Forest | **$45.43** | 0.426 |
| Gradient Boosting | $46.37 | 0.400 |

### Key takeaway
Room type and distance from the city center are the strongest predictors of price. The model
explains under half the price variance (R² ~0.42–0.45) — this reflects that a meaningful part
of Airbnb pricing depends on factors outside this dataset (photos, exact desirability, host
reputation), not a flaw in the modeling approach. Residual analysis shows the model is most
accurate for typical listings and least accurate for high-priced outliers.

---

## 🚀 How to Run the Project

### Step 1: Clone repository
```
git clone https://github.com/dhirendra8392/eda-airbnb-nyc.git
```

### Step 2: Install dependencies
```
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Step 3: Open notebooks
```
jupyter notebook Air_bnb.ipynb
jupyter notebook Airbnb_Price_Prediction.ipynb
```

---

## 🎯 Skills Demonstrated

This project highlights:
```
Exploratory Data Analysis (EDA)
Data Cleaning
Data Visualization
Feature Engineering
Regression Modeling (Linear Regression, Random Forest, Gradient Boosting)
Cross-Validation & Model Evaluation
Statistical Insight Extraction
Business Insight Generation
```

---

## 👨‍💻 Author

**Dhirendra Sahani**
B.Tech — Electronics & Instrumentation Engineering
National Institute of Technology Agartala

📧 dhirendra8392@gmail.com
🔗 LinkedIn: https://linkedin.com/in/dhirendra-sahani-129b98265
💻 GitHub: https://github.com/dhirendra8392

---

## ⭐ Project Purpose

This project is part of my **Data Analyst portfolio**, demonstrating my ability to analyze
real-world datasets, extract meaningful insights, and build and evaluate predictive models
using Python.

