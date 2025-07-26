# 🌍 Week 2 – Greenhouse Gas Emission Prediction using Machine Learning

Hi there! 👋 This is my Week 2 project for the internship, where I worked on predicting *greenhouse gas (GHG) emissions* based on real-world supply chain data for U.S. industries.

The idea is to build a model that can estimate emission factors using various descriptive and quality-related metrics — helping us understand how different factors affect emissions in the supply chain.

---

## 📌 Objective

The goal of this project is to:
> Predict the *Supply Chain Emission Factors with Margins* using features like substance type, unit, data quality scores, and correlation metrics — with the help of a machine learning model.

---

## 📁 Dataset Details

- *File Name*: SupplyChainEmissionFactorsforUSIndustriesCommodities (1).xlsx
- *Sheet Used*: 2015_Summary_Industry
- *Target Column*: Supply Chain Emission Factors with Margins
- *Features Used*:
  - Substance
  - Unit
  - DQ ReliabilityScore
  - DQ TemporalCorrelation
  - DQ GeographicalCorrelation
  - DQ TechnologicalCorrelation
  - DQ DataCollection

---

## 🧹 Preprocessing Steps

Here’s how I cleaned and prepared the data:
- Removed rows with missing values in the target column
- Filled missing values in numeric features with median values
- Dropped duplicate rows
- Used LabelEncoder to convert Substance and Unit columns into numeric values

---

## 🔧 Model Used

- *Random Forest Regressor*
- I chose this model because it's robust, easy to interpret, and performs well on structured tabular data.
- Trained the model with 100 trees (n_estimators=100) and tested it on a 20% test split.

---

## 📊 Evaluation Metrics

After training, I evaluated the model using:

- *R² Score* – How well the model explains the variance in data  
- *RMSE (Root Mean Squared Error)* – How far predictions are from actual values

---

## 📈 Visualizations

The notebook includes the following plots to better understand the results:

- *Actual vs Predicted Emission Values*  
- *Histogram of Residual Errors*  
- *Feature Importance Plot* (to see which input features influenced the prediction the most)

You’ll find all plots inside the notebook.

---

## 💻 How to Run

Make sure you have these libraries installed:

```bash
pip install pandas numpy matplotlib scikit-learn openpyxl
