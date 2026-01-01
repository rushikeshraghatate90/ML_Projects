# 🌧️ Rainfall Prediction using Machine Learning

This project focuses on **predicting rainfall** using **machine learning techniques** applied to historical weather data.  
It demonstrates the complete ML workflow including **data preprocessing, exploratory data analysis (EDA), visualization, and model training**.

---

## 📌 Features

- Rainfall prediction using supervised machine learning
- Exploratory Data Analysis (EDA)
- Statistical visualization of weather features
- Correlation analysis between meteorological variables
- Clean and interpretable plots for insights

---

## 🗂 Project Structure
```
├── Rainfall_Prediction_Using_Machine_Learning.ipynb  
├── README.md  
├── images/  
│   ├── Boxplot of columns.png  
│   ├── Correlation Heat map.png  
│   ├── rainfall_distribution.png  
│   └── Distribution of columns of dataset.png  
```
---

## 📦 Requirements

Install the required dependencies:
```
pip install numpy pandas matplotlib seaborn scikit-learn
```
---

## 📊 Dataset

- Historical weather dataset
- Includes the following features:
  - Pressure
  - Maximum Temperature
  - Minimum Temperature
  - Average Temperature
  - Humidity
  - Wind Speed
  - Cloud Cover
  - Dew Point
  - Sunshine
- Target variable:
  - **Rainfall (Binary: 0 = No Rain, 1 = Rain)**

---

## 🔍 Exploratory Data Analysis (EDA)

EDA is performed to:
- Understand feature distributions
- Detect outliers
- Analyze relationships between weather variables
- Study factors influencing rainfall

---

## 📦 Boxplot Analysis (Outlier Detection)

The boxplots below show the distribution and presence of outliers for each numerical feature such as pressure, temperature, 
humidity, wind speed, cloud cover, dew point, and sunshine.

<img width="512" height="512" alt="Boxplot of columns" src="https://github.com/user-attachments/assets/e77a138c-96c3-4a71-a575-d2c4dcf01feb" />

**Insight:**
- Helps identify extreme values
- Useful for deciding outlier handling strategies

---

## 🔗 Correlation Heatmap

The correlation heatmap visualizes the **linear relationship between all features**, including rainfall.

<img width="512" height="512" alt="Correlation Heat map" src="https://github.com/user-attachments/assets/f660f9d5-6452-43d2-8cf3-ec92e3848214" />

**Key Observations:**
- Strong correlation among temperature-related features
- Rainfall shows positive correlation with humidity and cloud cover
- Sunshine is negatively correlated with rainfall

---

## 🌧️ Rainfall Distribution

This plot shows the distribution of the target variable (Rainfall).

<img width="512" height="512" alt="rainfall_distribution" src="https://github.com/user-attachments/assets/562d77c1-efa2-4604-92d4-b2c9f4b3e523" />

**Insight:**
- Indicates class balance / imbalance
- Important for selecting evaluation metrics

---

## 📈 Feature Distribution Analysis

The following plots show the **distribution of individual weather features** using histograms and density curves.

<img width="512" height="512" alt="Distribution of columns of dataset" src="https://github.com/user-attachments/assets/e8925aff-8494-44dd-9bd6-ee001037f328" />

**Insight:**
- Reveals skewness and spread of features
- Helps decide normalization or transformation methods

---

## 🧠 Model Building (Overview)

- Machine learning models trained on processed data
- Binary classification task (Rain / No Rain)
- Models evaluated using accuracy and classification metrics

---

## 🧪 Evaluation Summary

- Data-driven insights extracted through EDA
- Feature relationships guide model selection
- Visualizations help interpret model behavior

---

## ⚠ Notes

- Weather data may contain noise and missing values
- Correlation does not imply causation
- Model performance depends heavily on feature quality

---

## 🔮 Future Improvements

- Feature selection using correlation and importance
- Handle class imbalance using resampling
- Hyperparameter tuning
- Try advanced models (XGBoost, Random Forest)
- Deploy as a web app using Streamlit

---

## 👨‍💻 Author

Rushikesh Raghatate  
Computer Science | Machine Learning | Data Science  

