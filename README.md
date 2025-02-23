### **NYPD Call Analysis for Crime Hotspots Prediction and Response Optimization**

#### **Project Overview**
This project aims to enhance public safety by analyzing **NYPD emergency call data** and **weather conditions** to predict crime hotspots and optimize response times. By leveraging **machine learning models**, law enforcement agencies can proactively allocate resources to high-risk areas, improving response efficiency and reducing crime impact.

#### **Team Members**
- Heet Gala
- Hemanth Chowdary
- Mansi Gopani
- Kunal Ahhirao

---

## **Table of Contents**
- [Project Overview](#project-overview)
- [Dataset Summary](#dataset-summary)
- [Data Preprocessing](#data-preprocessing)
- [Modeling Approach](#modeling-approach)
- [Results and Analysis](#results-and-analysis)
- [Future Work](#future-work)
- [Installation & Usage](#installation--usage)
- [Project Structure](#project-structure)
- [Acknowledgments](#acknowledgments)

---

## **Dataset Summary**
The dataset consists of **7,050,127 observations** across **18 columns**, containing:
- **Incident details**: Borough, crime type, coordinates, timestamps
- **Response times**: Dispatch, arrival, and closure timestamps
- **Weather data**: Integrated with emergency call data to assess impact

A key focus was placed on analyzing the top **8-9 crime radio codes**, reducing the dataset to approximately **450,000 records** for targeted crime response analysis.

---

## **Data Preprocessing**
To ensure high-quality input for modeling, the following preprocessing steps were applied:

1. **Handling Missing Values** – Used imputation techniques where necessary.
2. **Formatting Dates and Times** – Standardized timestamps and extracted features like time of day and day of the week.
3. **Categorical Encoding** – One-hot encoding was used for categorical variables like boroughs and radio codes.
4. **Feature Engineering** – Created derived features such as:
   - **Rolling window features** (e.g., number of calls in the last 2 hours)
   - **Weather-influenced response variations**
5. **Normalization** – Applied **Min-Max scaling** to numerical variables for consistency.

---

## **Modeling Approach**
Various machine learning models were tested to predict crime hotspots and response times:

### **1. Regression Models**
- Lasso, Ridge, and ElasticNet for **predicting numeric crime levels**.

### **2. Time Series Models**
- **ARIMA** and **Prophet** were used to **capture crime trends and seasonal patterns**.

### **3. Ensemble Models**
- **Random Forest** and **XGBoost** were implemented to **enhance predictive accuracy**.

### **4. Neural Networks**
- **LSTMs** were explored for sequence modeling but required a larger dataset for optimal performance.

### **Best Performing Model**
- **Decision Tree Algorithm** achieved the **highest accuracy of 70%** for predicting response times.

---

## **Results and Analysis**
Key findings from the analysis include:

1. **Crime Type Impact**
   - "Assault" incidents had response times **10% longer** than other crimes.

2. **Borough-wise Differences**
   - Manhattan had **faster response times** (by ~5 minutes) compared to the Bronx.

3. **Weather Influence**
   - Response times increased under **severe weather conditions**.

4. **Time-based Trends**
   - Evening hours (8 PM - 12 AM) had **faster responses** (-2.13% time reduction) compared to daytime (8 AM - 4 PM).

---

## **Future Work**
1. **Enhancing Model Accuracy** – Improving feature selection and integrating real-time data.
2. **Real-Time Data Integration** – Incorporating live emergency call updates for dynamic response planning.
3. **Public Event Impact Analysis** – Studying how events affect emergency response times.
4. **Bias & Fairness Assessment** – Ensuring fairness in response predictions across different precincts.

---

## **Project Structure**
```
📂 NYPD-Crime-Prediction
│── 📄 README.md          # Project Documentation
│── 📄 requirements.txt   # Dependencies
│── 📄 aml_pro2.ipynb     # Main Jupyter Notebook
│── 📄 Report.ipynb       # Report with results
│── 📄 AML_final_Ppt.pptx # Presentation slides
│── 📄 project.txt        # Technical details
```

---

## **Acknowledgments**
This project was developed as part of an **Advanced Machine Learning course**, focusing on predictive modeling for **law enforcement applications**. Special thanks to **stakeholders and advisors** for their valuable insights.
