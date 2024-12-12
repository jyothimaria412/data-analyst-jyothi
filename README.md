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
  The dataset used is the Business Licence 2024 dataset for March. It contains information about various businesses including their type, license status, and other related details. This dataset is critical for analyzing business trends, compliance, and other useful information.
- Data Enriching
- I have started with Data enriching. I have a structured dataset and in this step, we used Amazon Athena to run a SQL query on a dataset stored in the AWS Data Catalog. The query counts the number of records where the business_type column equals "Office." This step ensures that the enriched dataset filtered and ready for further analysis or reporting.
This query was necessary to focus specifically on the "Office" business type. Data enrichment involves refining the data by filtering or transforming it to meet specific needs. By using this segment, we could prepare the dataset for detailed analysis relevant to business needs or reporting goals. It is found that there is a total count of 123 business license which is issued in the office type segment in Vancouver for 2024 for the month of March.

![image](https://github.com/user-attachments/assets/231f66db-8c25-41f5-9755-be47a16e9305)

- Data Protection

- In this step we have enabled for Data protection for our resources. We have ensured Confidentiality protection, Integrity protection and availability protection for all our S3 storage resources. Firstly, I have created back-up buckets for all the exciting storage buckets.
- 
  - Confidentiality Protection
  - To ensure data confidentiality, we applied server side encryption for all objects stored in the Amazon S3 bucket. Specifically, I used AWS Key Management Service (AWS KMS) for encryption, which provides security by managing encryption keys. The encryption key is identified by its unique ARN (Amazon Resource Name).
  - Key Management Sevice is created
  - ![image](https://github.com/user-attachments/assets/4d4f8395-bc0c-4686-a3df-9cab93256943)
  - Confidentiality Protection is enabled for S3 bucket
![image](https://github.com/user-attachments/assets/4592bd40-00a4-4fc2-95f7-a73df4a7e911)

- Data Governance
- Data Observability

# [Project 5: Data Quality Control]
