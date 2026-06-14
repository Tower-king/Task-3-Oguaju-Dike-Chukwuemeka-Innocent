📋 Project Overview

This project demonstrates structured querying and exploratory data analysis of an Emergency Room visits dataset using SQL. 
The dataset was imported into a SQLite database and queried to extract clinical and operational insights — including patient demographics, diagnosis frequency,
billing patterns, and physician workload.

📁 Files
File
Description

ER_Visits_1001_Rows.csv

Source dataset imported into SQLite

hospital.db

SQLite database containing the ER_Visits table

Spl_queries.sql

🔍 SQL Queries & Business Questions

1. Total Patient Count
   
   SELECT COUNT(*) AS TotalPatients
FROM ER_Visits;

How many patients visited the ER in total?

2. Patient Count by Gender

   SELECT Gender,
COUNT(*) AS PatientCount
FROM ER_Visits
GROUP BY Gender;

What is the gender distribution of ER patients?

3. Most Common Diagnoses

   SELECT Diagnosis,
COUNT(*) AS Frequency
FROM ER_Visits
GROUP BY Diagnosis
ORDER BY Frequency DESC;

Which conditions bring patients to the ER most frequently?

4. Average Wait Time

   SELECT AVG(WaitTime_Min) AS AverageWaitTime
FROM ER_Visits;

What is the average patient wait time in minutes?

5. Average Length of Stay

   SELECT AVG(LengthOfStay_Hrs) AS AvgLengthOfStay
FROM ER_Visits;

How long do patients stay in the ER on average?

6. Total Revenue by Diagnosis

   SELECT Diagnosis,
SUM(BillAmount) AS TotalRevenue
FROM ER_Visits
GROUP BY Diagnosis
ORDER BY TotalRevenue DESC;

Which diagnoses generate the most revenue?

7. Doctor Workload

   SELECT Doctor,
COUNT(*) AS PatientsSeen
FROM ER_Visits
GROUP BY Doctor
ORDER BY PatientsSeen DESC;

How many patients did each doctor attend to?

8. Critical Severity Cases

    SELECT *
FROM ER_Visits
WHERE Severity = 'Critical';

Which patients were classified as Critical on arrival?

9. Top 10 Highest Bills

    SELECT *
FROM ER_Visits
ORDER BY BillAmount DESC
LIMIT 10;

Which visits incurred the highest billing amounts?

10. Average Bill by Severity

    SELECT Severity,
AVG(BillAmount) AS AverageBill
FROM ER_Visits
GROUP BY Severity;

Does severity level correlate with billing amount?


💡 Key Insights

Asthma, Pneumonia, and Hypertension are the top three most frequent ER diagnoses — all manageable with preventive care and early intervention

Mild severity cases paradoxically carry the highest average billing ($608K) — suggesting resource-intensive workups even for lower acuity patients

Average wait time of 95 minutes is a significant operational concern — international benchmarks target under 60 minutes for non-critical cases

Average length of stay of 35.87 hours indicates most patients require overnight observation

Malaria and Gastroenteritis in the top 10 diagnoses reflects the Nigerian clinical context — conditions often underrepresented in Western AI training data

🔧 Tools Used

SQLite — relational database engine

DB Browser for SQLite — query execution and result visualisation

Microsoft Excel - for dataset

Part of the DecodeLabs Data Analytics Internship Portfolio
