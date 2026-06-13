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
How many patients visited the ER in total?

3. Patient Count by Gender
What is the gender distribution of ER patients?

5. Most Common Diagnoses
Which conditions bring patients to the ER most frequently?

7. Average Wait Time
What is the average patient wait time in minutes?

9. Average Length of Stay
How long do patients stay in the ER on average?

11. Total Revenue by Diagnosis
Which diagnoses generate the most revenue?

13. Doctor Workload
How many patients did each doctor attend to?

15. Critical Severity Cases
Which patients were classified as Critical on arrival?

17. Top 10 Highest Bills
Which visits incurred the highest billing amounts?

19. Average Bill by Severity
Does severity level correlate with billing amount?

📊 Key Query Results
Average Bill by Severity
Severity
Average Bill (USD)
Critical
$571,037.47
Mild
$608,252.02
Moderate
$601,859.16
Severe
$591,304.41

Diagnosis Frequency
Diagnosis
Count
Asthma
111
Pneumonia
108
Hypertension
106
Stroke
104
Heart Failure
99
Appendicitis
98
Gastroenteritis
97
Fracture
97
Malaria
91
Diabetes
90

Operational Metrics
Metric
Value
Average Wait Time
95.31 minutes
Average Length of Stay
35.87 hours
Total Diagnoses
10 categories
Attending Physicians
6 doctors

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
