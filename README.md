# data-analyst-jyothi
Overview of the Projects Completed
# [Project 1: Descriptive Analysis of the Business Licenses issues for the city of Vancouver for year 2024 
- Project Description
- In order to improve operations and decision-making through the use of big data, the City of Vancouver has numerous . Building a Data Analytic Platform (DAP) is the proper approach in this situation to transform the data into accurate and practical information and to offer significant insights for the city. For the analysis, we are collecting company license data for 2024.
- Project Title
- Objective
- Dataset
- ![Exploratory analysis](https://github.com/user-attachments/assets/973648d0-39fe-4bdc-ac46-dc077a9abb6d)

- Methodology
  - Data Collection and Preperation
  - Descriptive Statistics
  - Data Visualization
  - Survival Analysis
  - Insights and Findings
  - Conclusion
- Tools and Technologies
- Deliverables
 
# Project 2: Exploratory Analysis]
# Project 3: DAP Impementation
- Project Description
  
  -The dataset used is the Business Licence 2024 dataset for March. It contains information about various businesses including their type, license status, and other related details. This dataset is critical for analyzing business trends, compliance, and other useful information.
  
- Data Enriching
- I have started with Data enriching. I have a structured dataset and in this step, we used Amazon Athena to run a SQL query on a dataset stored in the AWS Data Catalog. The query counts the number of records where the business_type column equals "Office." This step ensures that the enriched dataset filtered and ready for further analysis or reporting.
This query was necessary to focus specifically on the "Office" business type. Data enrichment involves refining the data by filtering or transforming it to meet specific needs. By using this segment, we could prepare the dataset for detailed analysis relevant to business needs or reporting goals. It is found that there is a total count of 123 business license which is issued in the office type segment in Vancouver for 2024 for the month of March.

![image](https://github.com/user-attachments/assets/231f66db-8c25-41f5-9755-be47a16e9305)

- Data Protection

- In this step we have enabled for Data protection for our resources. We have ensured Confidentiality protection, Integrity protection and availability protection for all our S3 storage resources. Firstly, I have created back-up buckets for all the exciting storage buckets.
- 
  Confidentiality Protection
  - To ensure data confidentiality, we applied server side encryption for all objects stored in the Amazon S3 bucket. Specifically, I used AWS Key Management Service (AWS KMS) for encryption, which provides security by managing encryption keys. The encryption key is identified by its unique ARN (Amazon Resource Name).
  - Key Management Sevice is created
  - 
  - ![image](https://github.com/user-attachments/assets/4d4f8395-bc0c-4686-a3df-9cab93256943)
  - 
  - Confidentiality Protection is enabled for S3 bucket
  - 
  - ![image](https://github.com/user-attachments/assets/4592bd40-00a4-4fc2-95f7-a73df4a7e911)

Integrity Protection

  -To ensure data integrity, we enabled Bucket Versioning for the S3 bucket. This feature helps us to maintain multiple versions of an object and also helps to ensure that previous versions can be retrieved in case of accidental deletions or overwrites

Integrity protection enabled for the s3 bucket

  -![image](https://github.com/user-attachments/assets/0438569a-54a6-44b2-919e-09ad4b44db3e)

Availability Protection

-To ensure data availability, implemented Replication Rules in the S3 bucket. The Replication Rule replicates the data to a backup bucket in the same region which help us to ensure the redundancy and high availability of data in case of system failures. The Replication Rule creates a backup copy of the data, protecting against data loss and ensuring that the data always remains accessible. We have created replication rules for all the buckets.

Availability protection enabled for the s3 bucket
 
  -![image](https://github.com/user-attachments/assets/b0910362-217d-4a5f-9a0e-d74a73f053dd)

Data Governance

- The Visual ETL (Extract, Transform, Load) workflow in AWS Glue is used for processing our data from city of Vancouver for the Business licenses year 2024 for the month of March. As part of the data governance process,  used the workflow which ensures data quality by validating the uniqueness and completeness of the data. Records that meet these quality checks are sent to the "Passed" folder in an S3 bucket, while those that do not meet the standards are moved to the "Failed" folder. This segregation helps maintain data integrity and ensures that only high-quality, reliable data is processed further.
  
Data Governance throgh ETL
- ![image](https://github.com/user-attachments/assets/06a75ee5-1eb5-42db-b5b3-6b7313b83455)

- Data Observability
- 
- To improve data observability, I used Amazon CloudWatch to create a dashboard that shows important metrics like bucket size, the number of objects stored, and estimated storage costs. As seen in the screenshot, the dashboard provides a clear view of these metrics, making it easier to monitor data usage. Logs are also turned on for each object to quickly identify and fix any issues. This ensures that the data storage and processing systems run smoothly with minimal downtime or errors.
Dashboard for the Objects
- ![image](https://github.com/user-attachments/assets/88eb3b7b-af5d-4e91-9bad-a555724dfc21)
- ![image](https://github.com/user-attachments/assets/67adb151-9c1c-4788-b0a3-4e17eac77b3a)



# [Project 5: Data Quality Control]
