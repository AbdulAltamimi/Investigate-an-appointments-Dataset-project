# 🏥 Investigate a Dataset: No-show Appointments in Brazil

This project analyzes a dataset of **100,000+ medical appointments in Brazil** to understand what factors influence whether patients **attend or miss** their scheduled appointments.  
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

Missed medical appointments are a major challenge for healthcare systems — they cause inefficiencies, lost time, and wasted resources.  
This analysis explores which patient characteristics (age, health conditions, SMS reminders, etc.) are linked to **attendance or absence** at appointments.

---

## 📊 Dataset Description

The dataset includes **110,527 medical appointments** from Brazil and contains the following features:

| Feature | Description |
|----------|-------------|
| `PatientId` | Unique patient identifier |
| `AppointmentID` | Appointment identifier |
| `Gender` | Patient gender |
| `ScheduledDay` | Date when the appointment was booked |
| `AppointmentDay` | Date of the appointment |
| `Age` | Patient’s age |
| `Neighbourhood` | Medical facility location |
| `Scholarship` | Enrolled in Bolsa Família welfare program (0 = No, 1 = Yes) |
| `Hipertension` | Patient has hypertension |
| `Diabetes` | Patient has diabetes |
| `Alcoholism` | Patient has history of alcoholism |
| `Handcap` | Disability indicator |
| `SMS_received` | Received SMS reminder (0 = No, 1 = Yes) |
| `No-show` | Whether the patient missed the appointment ("Yes" = missed, "No" = attended) |

---

## 🎯 Questions for Analysis

1. **What characteristics do most diabetic patients have?**  
2. **Is there a difference in attendance rate considering age, scholarship status, and SMS reminders?**

---

## 🧼 Data Wrangling

- Converted date columns (`ScheduledDay`, `AppointmentDay`) to datetime format.  
- Removed unrealistic values (e.g., negative ages).  
- Verified there were no missing or duplicate rows.  
- Optimized column types to reduce memory usage.  

---

## 🔍 Exploratory Data Analysis (EDA)

### 1️⃣ Characteristics of Diabetic Patients

#### Gender Distribution of Diabetic Patients
> Females diagnosed with diabetes slightly outnumber males (~2% difference).

<p align="center">
  <img src="images/diabetes_by_gender.png" alt="Diabetes by Gender" width="600">
</p>

#### Co-occurrence with Hypertension
> **81.7%** of diabetic patients also have hypertension, showing a strong correlation between the two diseases.

<p align="center">
  <img src="images/diabetes_hypertension.png" alt="Diabetes and Hypertension" width="600">
</p>

#### Age Distribution of Diabetic Patients
> Most diabetic patients are between **50 and 75 years old**.

<p align="center">
  <img src="images/diabetes_age_distribution.png" alt="Diabetes by Age" width="600">
</p>

#### Other Co-morbidities
> Only hypertension shows a strong link with diabetes; alcoholism and disability rates are low.

<p align="center">
  <img src="images/other_diseases_with_diabetes.png" alt="Other Diseases with Diabetes" width="600">
</p>

---

### 2️⃣ Appointment Attendance Analysis

#### SMS Reminder Effect
> Patients who received SMS reminders were **more likely to miss** their appointments.

<p align="center">
  <img src="images/attendance_by_sms.png" alt="Attendance by SMS" width="600">
</p>

#### Scholarship Effect
> Patients **without scholarships** had higher attendance rates.

<p align="center">
  <img src="images/attendance_by_scholarship.png" alt="Attendance by Scholarship" width="600">
</p>

#### Combined Effects (Scholarship + SMS)
> The lowest attendance rate was observed among patients who had **both a scholarship and received SMS reminders**.

<p align="center">
  <img src="images/attendance_by_factors.png" alt="Attendance by Factors" width="600">
</p>

---

## 📈 Key Findings

| Question | Insights |
|-----------|-----------|
| **1. Characteristics of diabetic patients** | Most diabetic patients are aged **50–75** and have **hypertension**. |
| **2. Attendance rate factors** | SMS reminders and scholarships both correlate with **lower attendance**. Patients without either factor are **most likely to attend**. |

---

## 🏁 Conclusion

1. **Diabetic Patients:**  
   - Older patients (50–75) with hypertension are most likely to have diabetes.  

2. **Appointment Attendance:**  
   - SMS reminders and scholarship programs **do not improve attendance**.  
   - Those without these factors are the **most reliable attendees**.  
   - Possible reasons: ineffective SMS content/timing or socio-economic barriers among scholarship participants.
