# 🌾 Sugarcane Production Analysis Project

This project is part of the **GeeksforGeeks Data Analysis Course**. It presents a detailed Exploratory Data Analysis (EDA) of global sugarcane production. The objective is to explore key metrics such as production volume, land usage, and yield per hectare across different countries and continents, to derive insights that support better agricultural strategies and resource management.

---

## 📊 Project Overview

- **Objective**: Analyze global sugarcane production.
- **Focus Areas**:
  - Production volume
  - Acreage (land usage)
  - Yield efficiency (Kg/Hectare)
  - Country-wise & Continent-wise comparison
- **Outcome**: Identify patterns, outliers, and correlations for better agricultural insights.

---

## 🧹 Data Cleaning

### 1. Remove Unwanted Characters
- Removed periods `.` from `Production(Tons)` and `Acreage(Hectare)`
- Replaced commas `,` with periods `.` in `Production_per_person(Kg)`

### 2. Drop Unnecessary Columns
- Dropped `Unnamed: 0` column using `df.drop(axis=1)`

### 3. Rename Columns
| Old Name                     | New Name                    |
|-----------------------------|-----------------------------|
| Production (Tons)           | Production(Tons)            |
| Production per Person (Kg)  | Production_per_person(Kg)   |
| Acreage (Hectare)           | Acreage(Hectare)            |
| Yield (Kg/Hectare)          | Yield(Kg/Hectare)           |

### 4. Handle Missing Values
- Dropped rows with missing values in `Acreage(Hectare)` and `Yield(Kg/Hectare)`
- Reset DataFrame index

### 5. Data Type Conversion
- Converted all relevant columns to `float` for analysis

---

## 📈 Univariate Analysis

### 1. Country Count by Continent

| Continent       | Countries Producing Sugarcane |
|----------------|-------------------------------|
| Africa          | 38                            |
| Asia            | 25                            |
| North America   | 22                            |
| South America   | 11                            |
| Oceania         | 4                             |
| Europe          | 2                             |

### 2. Distribution Analysis (via Histograms)
Analyzed distribution for:
- `Production(Tons)`
- `Production_per_person(Kg)`
- `Acreage(Hectare)`
- `Yield(Kg/Hectare)`

📌 Key Insights:
- Highly skewed production due to Brazil, India, China
- Wide variation in yield and production per person

### 3. Outlier Detection (via Boxplots)
- Major outliers identified in production and yield
- High-yielding countries stood out clearly

### 4. Violin Plot
- Plotted for `Production(Tons)` to understand spread, skewness, and outliers

---

## 📊 Bivariate Analysis

### 1. Top 15 Countries by Acreage
- Brazil, India, and China lead in land usage

### 2. Highest Yielding Country
- Guatemala had the highest `Yield(Kg/Hectare)`

### 3. Highest Production per Person
- Paraguay leads in `Production_per_person(Kg)`

### 4. Correlation Matrix (Heatmap)
| Variables                             | Correlation |
|--------------------------------------|-------------|
| Production(Tons) vs Acreage(Hectare) | **0.997**   |
| Production(Tons) vs Yield            | 0.132       |

### 5. Scatter Plots
- **Acreage vs Production**: Strong positive trend
- **Yield vs Production**: Weak correlation

---

## 🌍 Continental Analysis

### 1. Total Production by Continent
- **South America**: Highest (led by Brazil)
- **Asia**: Second
- **Africa**: Third

### 2. Impact of Country Count
- Fewer countries (e.g., in South America) can still lead in production if major producers are present.

---

## ✅ Conclusion

This analysis provided a detailed understanding of sugarcane production patterns around the world. The findings highlight:
- Disparity in production among countries
- Importance of acreage over yield in determining production volume
- Strong regional patterns, with South America and Asia leading globally

🔍 These insights can help refine agricultural strategies, optimize land use, and improve yield efficiency.

---

## 🛠️ Tools & Libraries Used

- Python (Pandas, Matplotlib, Seaborn)
- Jupyter Notebook
- GeeksforGeeks Data Analysis Curriculum

---

## 📌 Author

**Dilkhush Yash**  
*Data Analysis Enthusiast | B.Tech CSE | GFG Learner*

---
