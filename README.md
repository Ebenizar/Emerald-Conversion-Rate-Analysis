# UnitedHealthcare Claims Fraud Detection Analysis


### Table Of Content
[Background](#background)

[Problem Statement](#problem-statement)

[Analysis Objectives](#analysis-objectives)

[Data Description](#data-description)

[Tools Used](#tools-used)

[Data Cleaning Process](#data-cleaning)

[Data Analysis](#data-analysis)

[Key Insights](#key-insights)

[Business Recommendation](#business-recommendation)

## Background
This project focuses on designing an interactive healthcare insurance fraud analytics dashboard that enables insurance stakeholders to monitor claims activities, identify suspicious claims patterns, evaluate provider risks, and estimate financial exposure caused by potentially fraudulent activities. The dashboard will leverage healthcare claims data to support operational monitoring, fraud detection, and strategic decision-making through interactive visual analytics.

## Problem Statement
UnitedHealthcare insurance organizations process thousands of claims daily, making it increasingly difficult to manually detect fraudulent, duplicate, or suspicious claims. Fraudulent activities such as duplicate submissions, excessive billing, unusual provider behavior, delayed submissions, and abnormal claim patterns can result in significant financial losses and operational inefficiencies. Without an effective monitoring solution, UnitedHealthcare may struggle to:
- Detect high-risk claims in real time
- Monitor provider billing behavior effectively
- Identify duplicate claims and operational anomalies
- Reduce financial losses associated with fraud
- Improve operational transparency and risk management

## Analysis Objective
This project aims to develop a centralized dashboard that supports fraud detection, operational monitoring, provider
risk assessment, and strategic business intelligence.

## Data Description
UnitedHealthcare insurance claims dataset contains operational and financial claims information. The dataset includes the following fields:
- Claim ID (Unique identifier for each claim)
- Provider ID (Unique identifier for healthcare provider)
- Patient ID (Unique identifier for patient)
- Claim Date 9Date the claim was submitted)
- Department Medical department associated with claim
- Diagnosis Code (Diagnosis classification code)
- Procedure Code (Medical procedure/service code)
- Claim Amount (Amount billed by provider)
- Approved Amount (Amount approved by insurer)
- Submission Channel (Channel used to submit claim)
- Claim Status (Approved or Rejected)
- Days to Submit (Number of days taken to submit claim)
- Duplicate Flag (Indicates whether claim is duplicate)

## Tools 
- Excel
- Formulas & Functions

## Data Cleaning
The data cleaning process involves a rigorous process o
- Identifying and removing Duplicate, essentially from the Primary key column
- Date Cleaning
- Ensuring proper data type
- Data Normalization of text fields
- Calculating average of numerical fields to fill up blanks rows
The date field contained mixed date formats, unidentified date type, numerical and text Date format. To clean this data,
- Firstly, I had to duplicate the data so as to preserve the original copy
- Convert the date field data type to date
- Used IF and ISNUMBER function to seperate undentified date format into a new column for proper cleaning
- Used the LEFT, MID, and RIGHT functions to seperate month, day and year into seperate columns
- Joined month, day and year into a new colum in the appropriate format.
- Finally, joijned initially identified date to this newly cleaned date using the IF, ISNUMBER function

## Data Analysis
I loaded this clean data into Excel, and used Pivot table to summerize this data. This data summerization provided me with insight into the objective of this analysis. Using the pivot table, i carried out an exploratory data analysis to extract the following information:
- Duplicate Claim Rate
- Total no of Duplicate fflag
- Total Suspicious Claim amount, and potential loss to fraud activities
- Total Approved Claim
- Claims MoM Growth rate
- Top 10 Claim Submission by Fraud Flag
- Top 10 Average Claims Submission Lag Days by Providers
- Top 10 Provider Claim Submission by Claim Status
- Top 10 Average Claims Submission Lag Days by Providers
- Which providers exhibit unusual billing behavior?
- Does delayed submission correlate with claim rejection?
- Submission channels highest suspicious claim rates
- Financial impact of potentially fraudulent claims

## Key Insights
The fraud analysis uncovered several high-risk patterns that could significantly impact claims integrity and financial performance:

- 39% of all claims were flagged as potential duplicates, indicating a high likelihood of fraudulent submissions or claim processing inefficiencies.
- Potential financial exposure of ₦986.18K was identified from duplicate claims, highlighting the need for stronger fraud prevention controls.
- PRV_49 and PRV_63 consistently exhibited abnormal sbilling behavior across multiple peak months, making them high-priority providers for audit and investigation.
- PRV_86 recorded one of the highest duplicate claim rates, suggesting possible coordinated fraudulent activity.
- May, September, and November experienced unusually high claim submission volumes, revealing seasonal anomalies consistent with potential upcoding and fraudulent billing patterns.
- Online and mobile claim submission channels accounted for the majority of fraud-flagged claims, exposing vulnerabilities within digital claim submission processes.
- The dashboard successfully transformed fragmented claims data into a centralized fraud monitoring solution, enabling earlier identification of suspicious providers, billing anomalies, and financial risk.

## Business Recommendation
Based on the analysis, the following recommendations were proposed to strengthen fraud prevention and improve claims governance:

- Strengthen access controls by implementing Multi-Factor Authentication (MFA) across all digital claims submission platforms to reduce unauthorized access.
- Automate duplicate claim detection through real-time validation and alert systems to identify and prevent duplicate submissions before processing.
- Conduct targeted audits on high-risk providers, particularly PRV_49, PRV_63, and PRV_86, to investigate suspicious billing activities.
- Enhance provider verification by performing regular credential and licensing audits to eliminate inactive or fraudulent providers from the network.
- Introduce pre-authorization requirements for high-cost and high-risk medical procedures to reduce opportunities for upcoding and phantom billing.
- Implement continuous fraud monitoring using automated dashboards, anomaly detection, and periodic provider performance reviews to identify emerging fraud patterns.
- Improve claims data quality by enforcing standardized submission processes and stronger validation rules to enhance reporting accuracy and fraud detection
