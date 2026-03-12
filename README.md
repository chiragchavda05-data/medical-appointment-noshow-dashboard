# 🏥 medical-appointment-noshow-dashboard

A multi-page **Power BI dashboard project** built to analyze patient appointment attendance patterns and identify the key factors influencing missed medical appointments.

---

## 📌 Project Overview

Missed appointments are a major operational challenge in hospitals and clinics. When patients do not show up for scheduled appointments, it leads to wasted doctor time, underutilized healthcare resources, scheduling gaps, and delays in patient care.

This project uses the **Medical Appointment No-Show** dataset to build a **3-page interactive Power BI dashboard** that helps analyze attendance behavior and uncover important no-show drivers such as waiting time, SMS reminders, age group, neighbourhood, and patient health conditions.

---

## ❗ Problem Statement

Hospitals and healthcare centers often struggle to understand why patients miss scheduled appointments. Without a structured analytics dashboard, it becomes difficult to identify:

- High-risk patient segments
- Operational inefficiencies
- Location-based attendance patterns

The lack of actionable insights can result in:

- Inefficient scheduling
- Lower resource utilization
- Increased service delays
- Poor patient management decisions

---

## 🎯 Purpose of the Project

The purpose of this project is to transform raw appointment data into meaningful healthcare insights through a Power BI dashboard that can support better operational and administrative decision-making.

---

## ❓ Business Questions Answered by the Dashboard

This dashboard is designed to answer questions such as:

- How many total appointments were scheduled?
- What percentage of appointments were missed?
- Which age groups have higher missed appointments?
- Does receiving an SMS reminder reduce no-show behavior?
- Do factors like diabetes, hypertension, alcoholism, scholarship, or handicap affect attendance?
- How does waiting time influence appointment attendance?
- Which neighbourhoods have the highest missed appointments?
- On which weekdays are missed appointments more common?
- Which patient segments should healthcare administrators monitor more closely?

---

## 💡 Proposed Solution

A **3-page Power BI dashboard** was developed to analyze appointment attendance trends and identify the major drivers behind patient no-shows.

The solution provides:

- An overall appointment overview
- Factor-wise driver analysis
- Operational and segment-level insights

This helps healthcare administrators improve appointment planning, identify risky patterns, and support more data-driven actions.

---

## 🗂️ Dataset Information

- **Dataset Name:** Medical Appointment No-Show Dataset
- **Rows:** 110,527
- **Columns:** 14
- **Format:** CSV

### Main Raw Columns

- PatientId
- AppointmentID
- Gender
- ScheduledDay
- AppointmentDay
- Age
- Neighbourhood
- Scholarship
- Hipertension
- Diabetes
- Alcoholism
- Handcap
- SMS_received
- No-show

---

## 🧹 Data Cleaning and Preparation

The raw dataset was cleaned and transformed in **Power Query** before dashboard development.

### Cleaning Steps Performed

- Renamed columns for better readability:
  - `Hipertension` → `Hypertension`
  - `Handcap` → `Handicap`
  - `SMS_received` → `SMSReceived`
  - `No-show` → `NoShow`
- Removed invalid rows where `Age < 0`
- Created `WaitDays` using `AppointmentDay - ScheduledDay`
- Removed rows where `WaitDays < 0`
- Converted binary columns into readable flag columns:
  - ScholarshipFlag
  - HypertensionFlag
  - DiabetesFlag
  - AlcoholismFlag
  - HandicapFlag
  - SMSReceivedFlag
- Created `AttendanceStatus` from `NoShow`
  - `Yes` → `Missed`
  - `No` → `Attended`
- Created `AgeGroup` for demographic analysis
- Created `WaitBucket` for waiting time analysis
- Created weekday-based columns for trend analysis
- Removed unwanted raw identifier columns from the final dashboard view

---

## 🛠️ Tools and Technologies Used

- **Power BI Desktop**
- **Power Query**
- **DAX**
- **CSV Dataset**
- **GitHub** for project documentation and sharing

---

## ⚙️ Dashboard Development Process

The dashboard was developed in Power BI using a structured workflow:

1. The raw CSV dataset was imported into Power BI.
2. Data cleaning and transformation were performed in Power Query.
3. Invalid and inconsistent records were removed.
4. New analytical columns such as `AgeGroup`, `WaitDays`, `WaitBucket`, and `AttendanceStatus` were created.
5. DAX measures were developed for KPIs such as total appointments, missed appointments, no-show rate, average wait days, and distinct neighbourhoods.
6. A 3-page interactive dashboard was designed to present overview metrics, no-show drivers, and operational insights.
7. Slicers, charts, cards, and summary tables were used to make the dashboard interactive and decision-oriented.

---

## 📊 Dashboard Structure

The project contains **3 interactive dashboard pages**:

### 1️⃣ Overview

This page provides a summary of the appointment system.

**Includes:**

- Total Appointments
- Missed Appointments
- Attended Appointments
- No-Show Rate %
- Average Wait Days
- Attendance Split
- Gender vs Attendance
- Age Group Analysis
- Weekday Attendance Trend
- Top 10 Neighbourhoods by Missed Appointments

### 2️⃣ No-Show Drivers

This page focuses on the major factors that influence missed appointments.

**Includes:**

- SMS Reminder Effect
- Scholarship Effect
- Hypertension Effect
- Diabetes Effect
- Alcoholism Effect
- Handicap Effect
- Waiting Time Effect

### 3️⃣ Operational and Segment Insights

This page supports deeper operational analysis for administrators.

**Includes:**

- Top neighbourhoods by missed appointments
- Missed appointments by weekday
- Missed appointments by age group
- Average waiting time by age group
- Neighbourhood performance summary table

---

## 📈 Key KPIs

The following KPI measures were created using DAX:

- Total Appointments
- Missed Appointments
- Attended Appointments
- NoShow Rate %
- Avg Wait Days
- Avg Age
- Distinct Neighbourhoods

---

## 🔍 Key Insights

Some important insights generated from the dashboard include:

- Around **20.2%** of appointments were missed.
- The dataset contains over **110K appointments**, making the analysis more reliable.
- Waiting time shows a strong relationship with attendance behavior.
- Missed appointments vary across neighbourhoods, which can help identify location-level risk areas.
- Attendance patterns differ by age group and weekday.
- Patient-related factors such as scholarship status, hypertension, diabetes, alcoholism, and SMS reminders can be compared to understand their impact on attendance.

---

## 📁 Project Structure

```text
medical-appointment-noshow-dashboard/
│
├── medical_appointment_dashboard.pbix
├── medical_appointment_noshow_raw.csv
├── overview.png
├── no_show_drivers.png
├── operational_insights.png
└── README.md
```
## 📥 How to Clone This Repository

If someone wants to copy this project to their local system, they can clone the repository using Git.

### Step 1: Copy the repository link

Go to the GitHub repository and copy the repository URL.

**Example:**

```bash
https://github.com/your-username/medical-appointment-noshow-dashboard.git
```
### Step 2: Open Terminal or Git Bash

Open any one of the following:
Command Prompt
PowerShell
Git Bash
VS Code Terminal

### Step 3: Run the clone command
```
git clone https://github.com/chiragchavda05-data/medical-appointment-noshow-dashboard.git
```
### Step 4: Move into the project folder
```
cd medical-appointment-noshow-dashboard
```
### Step 5: Open the project

Open the .pbix file in Power BI Desktop
Make sure the .csv file is present in the same folder
If Power BI asks for file path refresh, reconnect the CSV file

 ## ✅ **Outcome**

This project successfully transformed raw healthcare appointment data into a structured and interactive business intelligence dashboard.  

It helps identify missed appointment trends, operational risks, and patient behavior patterns.  

These insights can support better healthcare scheduling, resource planning, and decision-making.  


 ## 🚀 **Future Scope**

This project can be extended further by:

- Adding predictive modeling for no-show risk  
- Integrating real-time hospital scheduling data  
- Including doctor-wise and department-wise appointment analytics  
- Adding patient communication strategy analysis  
- Building an alert-based risk monitoring system  


## 👨‍💻  **Author**

**Chirag Chavda**  

 ## 📜 **License**
This project is created for learning, academic, and portfolio purposes.

