# 🚗💰 Belarus Car Price Prediction

This project aims to **predict used car prices in Belarus** using machine learning models based on various vehicle features such as make, year, engine type, mileage, transmission, color, and more. The goal is to assist sellers and buyers in understanding the fair market value of used cars.

---

## 📊 Dataset Overview

- **Total Records**: 56,244  
- **Total Features**: 12  
- **Target Variable**: `price USD`  
- **Data Source**: [Kaggle](https://www.kaggle.com/)  
- **Problem Type**: Regression

### 🔑 Key Features

| Feature         | Description                            |
|-----------------|----------------------------------------|
| `make`          | Car brand (e.g., BMW, Toyota, Ford)    |
| `year`          | Year of manufacturing                  |
| `fuel type`     | Type of fuel (Petrol, Diesel, Electric)|
| `mileage`       | Distance driven in kilometers          |
| `transmission`  | Gearbox type (Manual/Automatic)        |
| `color`         | Color of the vehicle                   |
| `segment`       | Vehicle segment category               |
| `drive unit`    | Drive unit type (e.g., AWD, FWD)       |

---

## 🎯 Project Objectives

1. **Predict car prices** using various vehicle attributes.
2. **Analyze feature importance** to determine the most influential factors affecting price.
3. **Categorize car makes** into segments like:
   - 🏎️ Luxury European
   - 🚗 Asian
   - 🛻 American

---

## 🛠️ Tools & Technologies

- **Programming Language**: Python  
- **Data Handling**: Pandas, NumPy  
- **Visualization**: Matplotlib, Seaborn  
- **Modeling**: Scikit-learn  
- **IDE/Notebook**: Jupyter Notebook  

---

### ✅ Model Performance Summary

The **Decision Tree Regressor** model was used to predict car prices. The model achieved the following evaluation results:

- **R² Score**: `0.77`  
  > This indicates that **77% of the variance** in car prices can be explained by the model features. While this is a reasonably good fit, **23% of the variance remains unexplained**, indicating scope for improvement.

- **Mean Squared Error (MSE)**: `7,355,859.02`
- **Mean Absolute Error (MAE)**: `1869.24`
- **Root Mean Squared Error (RMSE)**: `2712.17`

> 🔎 **Interpretation**:
> - **RMSE** tells us that the model’s predictions deviate from the actual prices by about **2712.17 units** on average.
> - **MAE** indicates that the average absolute error is around **1869.24 units**.
> - The fact that **RMSE > MAE** suggests the presence of **some larger errors**, as RMSE penalizes larger deviations more heavily.

---

### 🔍 Feature Importance Analysis

The model also provides insight into how influential each feature is in predicting car price:

| Rank | Feature              | Importance Score |
|------|----------------------|------------------|
| 1    | **Year**             | `0.387`          |
| 2    | **Transmission**     | `0.320`          |
| 3    | **Mileage (km)**     | `0.168`          |
| 4    | **Engine Volume (cm³)** | `0.053`      |

> ⚠️ A common misconception was that **"Year and Engine Volume"** were the most important features.  
> ✅ The correct ranking based on model output is:
> - **Year**
> - **Transmission**
> - **Mileage**
> - **Engine Volume**

---

### 🧠 Conclusion

- ✅ The decision tree model explains approximately **77% of the variance** in car prices.
- 📉 Prediction errors are around **1869.24 units (MAE)** and **2712.17 units (RMSE)**.
- 🔍 The **most important features** influencing the car price are:
  1. **Year**
  2. **Transmission**
  3. **Mileage**
  4. **Engine Volume**

> ℹ️ **Note**: In decision trees, feature importance reflects the reduction in variance (impurity) due to that feature. A higher importance score means that the feature contributes more to improving prediction accuracy by influencing decision splits in the tree.
You can copy and paste this into a Markdown (.md) cell in your Jupyter Notebook. Let me know if you’d like this saved as a file!
