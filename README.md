# 🏥 Investigate a Dataset: No-show Appointments in Brazil

This project analyzes a dataset of **100,000 medical appointments in Brazil** to understand factors affecting whether patients **attend or miss** their scheduled medical appointments.  
It was completed as part of the **Udacity Data Analyst Nanodegree** program.

---

## 📋 Table of Contents
1. [Introduction](#introduction)  
2. [Dataset Description](#dataset-description)  
3. [Questions for Analysis](#questions-for-analysis)  
4. [Data Wrangling](#data-wrangling)  
5. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)  
6. [Key Findings](#key-findings)  
7. [Conclusion](#conclusion)  
8. [Files in Repository](#files-in-repository)  

---

## 🧠 Introduction

Missed medical appointments can disrupt hospital operations and waste valuable resources.  
This project aims to explore what factors influence a patient’s likelihood to **attend or miss** their medical appointment.  
The analysis focuses on relationships between patient characteristics (like age, gender, and health conditions) and attendance behavior.

---

## 📊 Dataset Description

The dataset contains **110,527 medical appointments** from Brazil and includes the following features:

| Feature | Description |
|----------|-------------|
| `PatientId` | Unique identifier for each patient |
| `AppointmentID` | Unique identifier for each appointment |
| `Gender` | Patient’s gender |
| `ScheduledDay` | Date when the appointment was booked |
| `AppointmentDay` | Date of the actual appointment |
| `Age` | Patient’s age |
| `Neighbourhood` | Location of the medical facility |
| `Scholarship` | Indicates if the patient is enrolled in the Bolsa Família welfare program |
| `Hipertension` | Whether the patient has hypertension |
| `Diabetes` | Whether the patient has diabetes |
| `Alcoholism` | Whether the patient has a history of alcoholism |
| `Handcap` | Whether the patient has a disability |
| `SMS_received` | Whether the patient received an SMS reminder |
| `No-show` | Whether the patient missed the appointment (“Yes” = missed, “No” = attended) |

---

## 🎯 Questions for Analysis

1. **What characteristics do most diabetic patients have?**  
2. **Is there a difference in attendance rate based on age, scholarship status, and SMS reminders?**

---

## 🧼 Data Wrangling

- Checked data types and converted relevant columns (`ScheduledDay`, `AppointmentDay`) to datetime.  
- Fixed incorrect or unrealistic values (e.g., removed negative ages).  
- Verified there were no missing or duplicate entries.  
- Optimized memory usage by converting binary columns to smaller integer types.  

---

## 🔍 Exploratory Data Analysis (EDA)

### 1️⃣ Diabetes and Related Factors
- Female diabetic patients slightly outnumber male diabetic patients (by ~2%).  
- About **81.7% of diabetic patients also have hypertension** — showing a strong correlation between the two diseases.  
- Most diabetic patients fall between **ages 50 and 75**.

### 2️⃣ Attendance Behavior
- Patients who **received SMS reminders were more likely to miss** their appointments.  
- Patients **without scholarships** were **more likely to attend** than those enrolled in the scholarship program.  
- The **lowest attendance rate** was among patients who had both a scholarship **and** received an SMS reminder.  

---

## 📈 Key Findings

| Question | Key Insights |
|-----------|--------------|
| **1. Characteristics of diabetic patients** | Most diabetic patients are between 50–75 years old and also have hypertension. |
| **2. Attendance rate differences** | SMS reminders and scholarship status both negatively correlate with attendance. Patients with neither are the most likely to attend. |

---

## 🏁 Conclusion

1. **For diabetic patients:**  
   The analysis suggests that older age (50–75) and hypertension are strong indicators of diabetes.  

2. **For attendance behavior:**  
   Contrary to expectations, sending SMS reminders or being part of a scholarship program does not improve attendance — it actually correlates with *lower* attendance rates.  
   This may indicate issues with SMS timing or content, or socioeconomic challenges related to scholarship recipients.

---

## 📂 Files in Repository
.
├── Investigate_a_Dataset.ipynb   # Main analysis notebook
├── Investigate_a_Dataset.html    # Exported HTML report
├── data/                         # Dataset (not included)
└── README.md                     # Project documentation
