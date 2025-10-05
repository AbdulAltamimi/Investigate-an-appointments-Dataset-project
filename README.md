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
- <img width="556" height="486" alt="image" src="https://github.com/user-attachments/assets/8a205c1d-b45e-4dc1-bf5d-3a33149880f6" />
- About **81.7% of diabetic patients also have hypertension** — showing a strong correlation between the two diseases.
- <img width="593" height="407" alt="image" src="https://github.com/user-attachments/assets/97b878d5-d128-4061-b024-ffb21dc8f7ae" />
<img width="557" height="525" alt="image" src="https://github.com/user-attachments/assets/3bcfb776-9dbf-4a8f-85a9-795285cfb481" />
- Most diabetic patients fall between **ages 50 and 75**.
- <img width="577" height="451" alt="image" src="https://github.com/user-attachments/assets/afaaa554-7fe5-40e6-a25f-37067ae7668d" />


### 2️⃣ Attendance Behavior
- Patients who **received SMS reminders were more likely to miss** their appointments.
- <img width="736" height="407" alt="image" src="https://github.com/user-attachments/assets/77b65b5a-7bd7-4e70-99eb-690155f80c03" />
<img width="656" height="404" alt="image" src="https://github.com/user-attachments/assets/7a3dcc34-c642-4289-8a88-9b5df12bc2e2" />
- Patients **without scholarships** were **more likely to attend** than those enrolled in the scholarship program.
- <img width="753" height="404" alt="image" src="https://github.com/user-attachments/assets/de2bc1b2-f00c-4450-8cf6-54473cf9203b" />
 <img width="712" height="408" alt="image" src="https://github.com/user-attachments/assets/1de85b67-7912-4f38-bafa-9fb9b3fd6184" />

- The **lowest attendance rate** was among patients who had both a scholarship **and** received an SMS reminder.  
<img width="608" height="539" alt="image" src="https://github.com/user-attachments/assets/6458a560-da48-4ed5-8c95-40593f5bd0f0" />

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

