# VitaTrack Wellness – Health Insights Dashboard 📊

VitaTrack Wellness is a digital health innovation company focused on enabling smarter lifestyle choices through data. This Power BI project analyzes user health metrics to uncover wellness patterns, identify risk factors, and suggest proactive lifestyle changes.

---

## Dataset

- **Source**: Provided by VitaTrack Wellness  
- **Features**:
  - ID, Age, Gender, Height (cm), Weight (kg), BMI
  - Daily Steps, Calories Intake, Hours of Sleep
  - Heart Rate, Blood Pressure
  - Exercise Hours per Week, Smoking Status
  - Alcohol Consumption per Week, Diabetic Status, Heart Disease

---

## Goals

- Understand lifestyle balance in terms of sleep, steps, and calories
- Identify risk factors for heart disease
- Explore the impact of habits like smoking and alcohol
- Visualize BMI trends across age and gender
- Segment users to recommend health improvements

---

## Dashboard Overview

The Power BI report contains **2 interactive sheets**:

---

### 🔵 Sheet 1: Lifestyle & Health Overview

| Visual | Type | Goal |
|--------|------|------|
| **1. Lifestyle Summary Cards** | KPI Cards | Display average steps, sleep hours, calories, BMI |
| **2. Donut Charts** | Donut Charts | Show distribution of Gender and Smoker status |
| **3. Lifestyle Balance Clustered Bar Chart** | Bar Chart | Compare average sleep, steps, and calorie intake |
| **4. Correlation Scatter Plot** | Scatter Plot | Visualize relationship between Sleep Hours and Daily Steps |
| **5. Heatmap Matrix** | Matrix | Analyze average Heart Rate & Blood Pressure by Smoking and Alcohol habits |
| **6. Slicers** | Filter Panel | Allow filtering by Age Group, Gender, Smoker, and Diabetic |

---

### 🔴 Sheet 2: Risk & Recommendation Analysis

| Visual | Type | Goal |
|--------|------|------|
| **1. Heart Disease by Age Group and Gender** | Stacked Column Chart | Identify high-risk demographics for heart disease |
| **2. BMI Distribution** |  Scatter Plot (Alt to Box Plot) | Show BMI by Age Group & Gender |
| **3. Heart Disease vs Lifestyle Habits** | Bar Chart | Display heart disease count for Smokers, Diabetics, and Alcohol Users |
| **4. Vital Stats Matrix** | Matrix | Show average Heart Rate & BP by Smoking and Alcohol bins |
| **5. Health Segment Clustering** | Scatter Plot | Segment users based on steps, exercise, and calorie intake |

---

## 🛠️ Features Used

- Power Query for data cleaning and binning
- DAX for KPIs and calculated fields
- Custom clustering via Analytics pane
- Smart Narrative for auto-generated summary
- Interactive slicers and filters

---

## 📌 Binning Example (Power Query)

```m
if [Alcohol_Consumption_per_Week] = 0 then "None" 
else if [Alcohol_Consumption_per_Week] <= 3 then "Low" 
else if [Alcohol_Consumption_per_Week] <= 6 then "Moderate" 
else "High"
