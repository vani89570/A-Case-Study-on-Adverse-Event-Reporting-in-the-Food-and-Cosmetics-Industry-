---
## 🍽️ Travel, Food & Beverages
# A Case Study on Adverse Event Reporting in the Food and Cosmetics Industry

---
Background
---
📊 The CAERS database is a critical tool for the FDA, containing adverse event and product complaint reports related to foods, dietary supplements, and cosmetics. This dataset, covering the period from 2004 to the second quarter of 2017, includes detailed records of various products and associated adverse events. Each record is meticulously coded using the Medical Dictionary for Regulatory Activities (MedDRA) terminology, ensuring standardized reporting across different products. The data captures elements like report numbers, product roles, brand names, industry codes, patient demographics, adverse outcomes, and coded symptoms.

![image](https://github.com/user-attachments/assets/3245876c-8d65-43dc-b1f9-36f60d769be0)

### Objective

The primary objective of analyzing the CFSAN Adverse Event Reporting System (CAERS) dataset is to gain a comprehensive understanding of adverse events associated with foods, dietary supplements, and cosmetics as reported to the FDA. This analysis aims to identify patterns and trends in these events, including:

- 📅 Distribution across different product categories.
- 🧑‍🤝‍🧑 Demographic characteristics of those affected.
- 🩺 Types and severities of reported symptoms and outcomes.
- By exploring these aspects, the analysis seeks to contribute valuable insights for enhancing product safety surveillance, informing regulatory policies, and ultimately improving public health outcomes by identifying potential risks and areas for intervention in the industries of food, dietary supplements, and cosmetics.
---
Data Source:
👉 CAERS_ASCII_2004_2017Q2.csv

---
The dataset from the CFSAN Adverse Event Reporting System (CAERS) is a comprehensive collection of reports submitted to the FDA regarding adverse events and product complaints associated with foods, dietary supplements, and cosmetics. It spans from 2004 to the second quarter of 2017 and includes several key fields:

---
- RA_Report #: A unique identifier for each adverse event report.
- RA_CAERS Created Date: The date when the report was entered into the CAERS database.
- AEC_Event Start Date: The date when the adverse event started.
- PRI_Product Role: Indicates whether the product was a suspect or concomitant (present during the event but not necessarily the cause).
- PRI_Reported Brand/Product Name: The name of the product reported to be associated with the adverse event.
- PRI_FDA Industry Code & Name: Categorization of the product based on FDA industry codes and names, such as 'Bakery Prod/Dough/Mix/Icing', 'Ice Cream Prod', etc.
- CI_Age at Adverse Event: Age of the individual experiencing the adverse event.
- CI_Age Unit: Unit of measurement for age (e.g., years, months).
- CI_Gender: Gender of the individual.
- AEC_One Row Outcomes: Describes the outcomes of the event, such as hospitalization, ER visit, or non-serious injuries/illness.
- SYM_One Row Coded Symptoms: Lists the symptoms reported in association with the adverse event.

---

### Part 1: Data Cleaning, Modeling, and DAX in Power BI
- Data Importing and Preliminary Analysis:
Import the dataset into Power BI and perform an initial examination. Identify any apparent inconsistencies or data quality issues.

- Handling Missing Values:
Investigate and address the missing values. Determine an appropriate strategy for handling these.
- Data Type Standardization:

Ensure that all data types are correctly identified and converted if necessary, particularly for dates and numerical fields.
- Product Role Categorization:

Categorize the products based on their role ('PRI_Product Role') and analyze the distribution of these roles in the dataset.
- FDA Industry Analysis:

Group the data by 'PRI_FDA Industry Name' and analyze the frequency of reports in each industry.
- Age Group Analysis:

Create age groups from 'CI_Age at Adverse Event' and analyze the distribution of adverse events across these age groups.
- Gender-Based Analysis:

Examine the distribution of reports by gender. Are there noticeable differences in adverse event reporting between genders?
- Adverse Event Start Date Analysis:

Analyze the distribution of 'AEC_Event Start Date' over time. Identify any trends or patterns.
- Outcome Categorization:

Categorize 'AEC_One Row Outcomes' into broader categories and analyze the distribution of these categories.
- Symptom Frequency Analysis:

Analyze the most frequently reported symptoms in 'SYM_One Row Coded Symptoms'.
- Correlation between Age and Symptom Types:

Use DAX to investigate if there's a correlation between age and types of symptoms reported.
- Industry and Outcome Relationship:

Examine the relationship between 'PRI_FDA Industry Name' and types of outcomes reported.
- Time Series Analysis of Reports:

Perform a time series analysis to identify any seasonal trends in report submissions.
- DAX for Advanced Age Analysis:

Utilize DAX to calculate the average, median, and mode of the ages at which adverse events occur.
- Product Name Analysis:

Use text analysis techniques to identify the most commonly reported products.
- Geographical Distribution (If Applicable):

If the data includes geographical information, analyze the distribution of reports by region.
- Advanced DAX: Report Frequency Calculation:

Develop a DAX formula to calculate the frequency of reports per month or year.
- Symptom Severity Index:

Create a severity index for symptoms based on their frequency and association with serious outcomes.
- Report Duplication Analysis:

Identify and handle any duplicate reports in the dataset.
- Predictive Modeling for Adverse Event Risk:

Use DAX to create a predictive model estimating the risk of adverse events based on product type and demographic data.
- Complex Symptom Pattern Analysis:

Utilizing nested functions in DAX, analyze the dataset to find patterns in the occurrence of symptoms. For instance, create a measure that identifies the frequency of certain symptoms occurring together in the same report.
- Advanced Outcome Prediction Model:

Develop an advanced predictive model using DAX that estimates the likelihood of severe outcomes based on multiple factors.

---
<img width="674" alt="Screenshot 2024-09-27 181724" src="https://github.com/user-attachments/assets/e6118249-6486-4d17-9ff6-1b6432266cd8">
<img width="698" alt="Screenshot 2024-09-27 181806" src="https://github.com/user-attachments/assets/5f0164c3-9993-4cd9-ac18-c55d347e3058">
<img width="710" alt="Screenshot 2024-09-27 181853" src="https://github.com/user-attachments/assets/a1e4e018-88dd-4927-b3aa-3482c7334e99">
<img width="676" alt="Screenshot 2024-09-27 181907" src="https://github.com/user-attachments/assets/88718d8b-c3f1-4722-a323-61f778bb7538">
<img width="674" alt="Screenshot 2024-09-27 181919" src="https://github.com/user-attachments/assets/474d7981-d2bd-419b-9fed-a375b108a6aa">
<img width="682" alt="Screenshot 2024-09-27 181933" src="https://github.com/user-attachments/assets/ca8e6471-25f2-48d2-85fb-ad30615d7fa6">
<img width="685" alt="Screenshot 2024-09-27 181943" src="https://github.com/user-attachments/assets/534b4311-01c4-4908-8037-88a91a186e09">
<img width="960" alt="Screenshot 2024-09-27 181953" src="https://github.com/user-attachments/assets/9a5a83f6-db93-4c3b-850a-a1b603734e99">
<img width="679" alt="Screenshot 2024-09-27 182016" src="https://github.com/user-attachments/assets/18e87406-f4b6-4172-86de-e69950332ab4">
<img width="690" alt="Screenshot 2024-09-27 182030" src="https://github.com/user-attachments/assets/d9f1c388-b1c1-468f-b2bc-4160e4eae236">
<img width="683" alt="Screenshot 2024-09-27 182044" src="https://github.com/user-attachments/assets/68b6e333-bb10-4702-94d4-b040bafa16c0">
<img width="709" alt="Screenshot 2024-09-27 182055" src="https://github.com/user-attachments/assets/ccc3e96e-bf34-4281-90b5-784df1fc0751">
<img width="695" alt="Screenshot 2024-09-27 182105" src="https://github.com/user-attachments/assets/7c2c2d21-7163-4ee4-a28e-9aa79c36b9ce">

---

### Part 2: Dashboard Building
- Adverse Event Reporting Dashboard:

Develop a comprehensive dashboard showcasing key metrics such as frequency of reports, common symptoms, product types, and demographic breakdowns. Include interactive filters for industry, product role, and age groups.
- Dashboard Design and Accessibility:

Focus on making the dashboard visually appealing, easy to navigate, and accessible to users with different levels of expertise.
- Time-Based Reporting Trends:- 

Incorporate a section in the dashboard to visualize trends in adverse event reporting over time, highlighting any notable patterns.
- Industry and Outcome Correlation Visualization:

Create an interactive visualization showing the correlation between different industries and reported outcomes.
- Demographic Analysis Section:

Implement a section in the dashboard dedicated to analyzing demographic data, including age and gender distributions.
- Key Insights and Data Storytelling:

Provide a section that summarizes key insights or trends identified in the data, using visual storytelling techniques to highlight important findings.

<img width="690" alt="Screenshot 2024-09-27 182118" src="https://github.com/user-attachments/assets/c73084c3-2966-403b-9ee4-0323d7bd9353">
<img width="685" alt="Screenshot 2024-09-27 182147" src="https://github.com/user-attachments/assets/0d0acbea-2345-4c6d-9a84-ba7bccba31d1">
<img width="680" alt="Screenshot 2024-09-27 182206" src="https://github.com/user-attachments/assets/055fd190-a960-4057-bf3a-47cb5b7f05b6">
<img width="541" alt="Screenshot 2024-09-27 182223" src="https://github.com/user-attachments/assets/1122c61f-597d-499f-b75a-7d3563889268">
