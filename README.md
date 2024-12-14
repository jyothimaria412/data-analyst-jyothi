# data-analyst-jyothi
# Overview of the Projects Completed
# Project 1: Descriptive Analysis of the Business Licenses issues for the city of Vancouver for year 2024 
- Project Description
   This descriptive analysis focuses on the filtered dataset of Business Licenses for the City of Vancouver in March 2024. It examines the proportion of total business licenses with the status "issued" for the 'Health Services' business type and compares it to the total licenses across all business types.
  The analysis aims to determine the relative share of 'Health Services' licenses, providing insights into licensing trends and assessing whether this sector plays a significant or minor role in the overall business licensing landscape.
  This information is valuable for identifying sector-specific growth and understanding the impact of 'Health Services' in Vancouver's business licenses.
- Objective
  To analyze the proportion of business licenses issued for the 'Health Services' business type in March 2024 compared to the total licenses across all business types. This project aims to understand the relative contribution of 'Health Services' to the overall business licensing landscape in Vancouver, identifying licensing trends and assessing the significance of this sector in the  city's business licenses.
  
- Dataset
  
  ![Exploratory analysis](https://github.com/user-attachments/assets/973648d0-39fe-4bdc-ac46-dc077a9abb6d)

- Methodology
  
    -  Data Collection and Preperation
  
    -  The below figure shows teh design diagram for the Data ingestion. The extracted data from the City of Vancouver Portal is ingested to teh S3 raw bucket and it is partioned as year 2024, March. The data is a structured data.
 
    ![image](https://github.com/user-attachments/assets/0b2b071d-fd3f-4626-a246-bb8b98b202df)
 
  The figure shows the dataset ingested to the bucket ‘bl-raw-jm’ further partitioned to the ingestion year 2024, and the month is March for the city of Vancouver.:
    
   ![image](https://github.com/user-attachments/assets/eb385f84-f398-4ebe-8fb8-f9febf873714)

  -  Data Profiling
      The data will be moved for profiling and then to cleaning through AWS Databrew, where data will be fetched for profiling for further analysis of data and will be cleaned accordingly. The cleaned and profiled data will be moved to another bucket which is called ‘bl-trf-jm’
    Diagram designed for Data Profiling and Cleaning
 
     ![image](https://github.com/user-attachments/assets/2dd95624-662b-499c-bb67-1c4d39871b22)
     
    Data Profile view
    
     ![image](https://github.com/user-attachments/assets/6b03dad0-2b36-4aeb-b3dd-d3624964504e)
  -  Data Cleaning
      We have cleaned the data and created the recipes based on our requirements. The data is already structured data, so there isn’t much transformation in this stage. Also, while creating the job, we have set the output data partitioned based on the column ‘Business Type’
     
     ![image](https://github.com/user-attachments/assets/425af4ea-d7e4-4bc5-84b5-6bb29d74ad6d)
     
  -  Data transformed to bl-trf-jm bucket
    
     ![image](https://github.com/user-attachments/assets/dc8ff842-cf27-4333-bb1b-24c05b1c5371)
     
      Data after the cleaning process was placed in the ‘bl-trf-jm’ bucket. Here we have partitioned the data based on the ‘Business type’ and ‘Status’
 - Data Pipeline Design Process
     ![image](https://github.com/user-attachments/assets/ff581b4d-8ba6-4007-b5cd-a51472ce8d05)
   
- Descriptive Statistics
    I have done the descriptive analysis based on proportion of business licenses issued for the "Health Services" business type relative to the total number of business licenses across all categories. This analysis will help us to understand the representation of the ‘Health Services’ sector compared to other business type under the status ‘Issued’.
  
- Proportion of business licenses issued for the "Health Services" business type calculation
  
  ![image](https://github.com/user-attachments/assets/5d8b90ec-7476-43ab-a6e4-7e1c3c190315)
  
- Insights and Findings
- 
  - Proportion of Health Services Licenses:
    For active licenses (status = Issued), 19 licenses were issued under the "Health Services" category.
  This accounts for approximately 9.85% of the total licenses issued across all business types.
  Inactive Licenses:
  For inactive licenses (status = Inactive), only 2 licenses were associated with the "Health Services" business type.
  This include a 50% proportion of the total inactive licenses, which is high for this category.

- ### Conclusion
   The analysis highlights a notable relationship between the number of licenses issued (count(businessType)) and the average fees paid (avg(feePaid)) by business types. Business types with higher license counts, such as "Office," generally exhibit moderate and uniform average fees, reflecting standardized licensing structures. In contrast, business types with lower license counts, like "Electrical Contractor," tend to have significantly higher average fees, possibly due to specialized requirements. Outliers, such as "Beauty Services," demonstrate high average fees despite fewer licenses, suggesting unique licensing or operational factors that merit further investigation.
The analysis reveals that in March 2024, the "Health Services" business type accounted for approximately 9.85% of all active business licenses (status = Issued) in the City of Vancouver. This indicates a moderate representation of the sector compared to other business types. Additionally, among inactive licenses, "Health Services" holds a significant proportion of 50%, highlighting potential areas for further investigation into sector-specific challenges or opportunities. This analysis provides a clear understanding of the role and performance of the "Health Services" sector within the overall business licensing landscape.

 
# Project 2: Exploratory Analysis]

- Objective: Do Business Types with Higher License Counts Have Lower Average Fees?
   As done in the descriptive analysis, data is ingested, then profiling and cleaning, and then data is analysed in the pipeline process as shown below.
- 
- Analysis of Business Licenses and Fees Paid by Business Type for March 2024
- 
  ![image](https://github.com/user-attachments/assets/f8d45849-b002-4781-90eb-035b1231010b)
  
- Data Pipeline Design
- 
  ![image](https://github.com/user-attachments/assets/f74958d3-4518-4d9b-ab9f-296b5c919a7d)
  
- The objective of this analysis is to explore the relationship between the number of licenses issued for a business type (count(businessType)) and the average fee paid (avg(feePaid)) by each business type. This is to identify patterns or trends such as whether business types with more licenses tend to pay lower average fees and highlight any outliers in the dataset
-  Insights and Findings
-  
  - Correlation Analysis

   To analyze the relationship between count(businessType) and avg(feePaid):
Trends Observed:
   Business types with higher license counts like ‘Office’ tend to have moderate average fees.
Some business types with low license counts like ‘Electrical Contractor’ have significantly higher average fees.
Patterns:
   Business types with higher counts typically have more uniform average fees, indicating standardized licensing fees.
Outliers exist where certain business types (e.g., "Beauty Services") have a low number of licenses but high average fees may be due to specialized requirements.
- ### Conclusion
   The analysis highlights a notable relationship between the number of licenses issued (`count(businessType)`) and the average fees paid (`avg(feePaid)`) by business types. Business types with higher license counts, such as "Office," generally exhibit moderate and uniform average fees, reflecting standardized licensing structures. In contrast, business types with lower license counts, like "Electrical Contractor," tend to have significantly higher average fees, possibly due to specialized requirements. Outliers, such as "Beauty Services," demonstrate high average fees despite fewer licenses, suggesting unique licensing or operational factors that merit further investigation.

# Project 3: DAP Impementation

- Project Description
  
  The dataset used is the Business Licence 2024 dataset for March. It contains information about various businesses including their type, license status, and other related details. This dataset is critical for analyzing business trends, compliance, and other useful information.

- Data Enriching
  
  I have started with Data enriching. I have a structured dataset and in this step, we used Amazon Athena to run a SQL query on a dataset stored in the AWS Data Catalog. The query counts the number of records where the business_type column equals "Office." This step ensures that the enriched dataset filtered and ready for further analysis or reporting.
This query was necessary to focus specifically on the "Office" business type. Data enrichment involves refining the data by filtering or transforming it to meet specific needs. By using this segment, we could prepare the dataset for detailed analysis relevant to business needs or reporting goals. It is found that there is a total count of 123 business license which is issued in the office type segment in Vancouver for 2024 for the month of March.
  Finding the total count of business type “Office”
  
  ![image](https://github.com/user-attachments/assets/231f66db-8c25-41f5-9755-be47a16e9305)

Data Protection

- In this step we have enabled for Data protection for our resources. We have ensured Confidentiality protection, Integrity protection and availability protection for all our S3 storage resources. Firstly, I have created back-up buckets for all the exciting storage buckets.
-
  - Confidentiality Protection
 - 
    - To ensure data confidentiality, we applied server side encryption for all objects stored in the Amazon S3 bucket. Specifically, I used AWS Key Management Service (AWS KMS) for encryption, which provides security by managing encryption keys. The encryption key is identified by its unique ARN (Amazon Resource Name).
  - 
  Key Management Sevice is created
    
 ![image](https://github.com/user-attachments/assets/4d4f8395-bc0c-4686-a3df-9cab93256943)
    
Confidentiality Protection is enabled for S3 bucket
    
![image](https://github.com/user-attachments/assets/4592bd40-00a4-4fc2-95f7-a73df4a7e911)

   - Integrity Protection

  - To ensure data integrity, we enabled Bucket Versioning for the S3 bucket. This feature helps us to maintain multiple versions of an object and also helps to ensure that previous versions can be retrieved in case of accidental deletions or overwrites

Integrity protection enabled for the s3 bucket

   ![image](https://github.com/user-attachments/assets/0438569a-54a6-44b2-919e-09ad4b44db3e)
    

  - Availability Protection

      - To ensure data availability, implemented Replication Rules in the S3 bucket. The Replication Rule replicates the data to a backup bucket in the same region which help us to ensure the redundancy and high availability of data in case of system failures. The Replication Rule creates a backup copy of the data, protecting against data loss and ensuring that the data always remains accessible. We have created replication rules for all the buckets.

Availability protection enabled for the s3 bucket
 
  ![image](https://github.com/user-attachments/assets/b0910362-217d-4a5f-9a0e-d74a73f053dd)

- Data Governance

  - The Visual ETL (Extract, Transform, Load) workflow in AWS Glue is used for processing our data from city of Vancouver for the Business licenses year 2024 for the month of March. As part of the data governance process,  used the workflow which ensures data quality by validating the uniqueness and completeness of the data. Records that meet these quality checks are sent to the "Passed" folder in an S3 bucket, while those that do not meet the standards are moved to the "Failed" folder. This segregation helps maintain data integrity and ensures that only high-quality, reliable data is processed further.
  
Data Governance throgh ETL

  ![image](https://github.com/user-attachments/assets/06a75ee5-1eb5-42db-b5b3-6b7313b83455)

- Data Observability
 
  - To improve data observability, I used Amazon CloudWatch to create a dashboard that shows important metrics like bucket size, the number of objects stored, and estimated storage costs. As seen in the screenshot, the dashboard provides a clear view of these metrics, making it easier to monitor data usage. Logs are also turned on for each object to quickly identify and fix any issues. This ensures that the data storage and processing systems run smoothly with minimal downtime or errors.
  
Dashboard for the Objects

  ![image](https://github.com/user-attachments/assets/88eb3b7b-af5d-4e91-9bad-a555724dfc21)
  ![image](https://github.com/user-attachments/assets/67adb151-9c1c-4788-b0a3-4e17eac77b3a)



# [Project 5: Data Quality Control]
