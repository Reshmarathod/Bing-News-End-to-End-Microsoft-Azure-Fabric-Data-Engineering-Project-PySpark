![image](https://github.com/Reshmarathod/Bing-News-End-to-End-Microsoft-Azure-Fabric-Data-Engineering-Project-Pyspark/assets/146751905/1391ca22-1ef3-4055-9546-212bc5ef800d)


## Bing News End-to-End Microsoft Azure Fabric Data Engineering Project

**Introduction**

This project aims to perform data analytics on news data obtained from the Bing News API utilizing various Microsoft Azure technologies. The process involves data ingestion, transformation, sentiment analysis, semantic modeling, and visualization using Azure Data Factory, Azure Databricks, Azure Synapse Analytics, and Power BI. The end goal is to provide actionable insights from news data and automate the dissemination of positive news articles through email triggers.

**Project Workflow**

### 1. Data Ingestion with Azure Data Factory

Utilized Azure Data Factory to ingest JSON data from the Bing News API into Lakehouse files folder. Azure Data 
Factory provides a robust platform for orchestrating and automating data workflows, ensuring reliable and scalable 
data ingestion.

 ![image](https://github.com/Reshmarathod/Bing-News-End-to-End-Microsoft-Azure-Fabric-Data-Engineering-Project-Pyspark/assets/146751905/95385307-387c-43d9-9f9b-45e73aec67ed)


![image](https://github.com/Reshmarathod/Bing-News-End-to-End-Microsoft-Azure-Fabric-Data-Engineering-Project-Pyspark/assets/146751905/cf80e417-3100-4a4a-8f78-1ba8f262a2ea)





### 2.Data Transformation with PySpark Notebook

Created a PySpark notebook to read the JSON data from the Lakehouse Files folder. Utilized the Explode() function 
to parse JSON object elements and extract necessary data into a dataframe. Implemented a type 1 incremental load 
using Spark SQL Merge Into to load data into a Delta table. Delta tables offer ACID transactions and time travel 
capabilities, ensuring data integrity and efficient data manipulation.

  [Pyspark Tranformation - 1](https://github.com/Reshmarathod/Bing-News-End-to-End-Microsoft-Azure-Fabric-Data-Engineering-Project-Pyspark/blob/main/Transformation-1.ipynb)



### 3. Sentiment Analysis with PySpark and Azure SynapseML

Developed a PySpark notebook to further analyze the Delta table created in the previous step. Utilized Azure 
SynapseML's AnalyzeText() function to perform sentiment analysis on the "description" data within the dataframe. 
Implemented type 1 incremental load with Merge Into to append sentiment analysis results to the Delta table.

   
  [Pyspark Tranformation - 2](https://github.com/Reshmarathod/Bing-News-End-to-End-Microsoft-Azure-Fabric-Data-Engineering-Project-Pyspark/blob/main/Transformation-2.ipynb)



 ![image](https://github.com/Reshmarathod/Bing-News-End-to-End-Microsoft-Azure-Fabric-Data-Engineering-Project-Pyspark/assets/146751905/7324485c-8f0a-455a-a348-dd37a00e9f41)




### 4. Semantic Modeling with Azure Synapse Analytics

Leveraged Azure Synapse Analytics to create a Semantic Model from the Delta table containing sentiment analysis 
data (tbl_sentiment_analysis). Extended the data model by adding new measures to calculate percentages of 
positive, negative, and neutral news articles. Semantic modeling provides a structured framework for organizing 
and analyzing data, enabling intuitive exploration and understanding of data insights.


  ![image](https://github.com/Reshmarathod/Bing-News-End-to-End-Microsoft-Azure-Fabric-Data-Engineering-Project-Pyspark/assets/146751905/66766399-513f-4bee-bff8-a568977e1666)



### 5. Data Visualization with Power BI

Developed a Power BI report to visualize the data from the Semantic Model. Utilized various visualizations such 
as tables, slicers, and cards to present key metrics and trends. Power BI enables interactive and insightful data 
exploration, empowering users to gain actionable insights from the data.

 ![image](https://github.com/Reshmarathod/Bing-News-End-to-End-Microsoft-Azure-Fabric-Data-Engineering-Project-Pyspark/assets/146751905/ac92555a-9997-4579-a418-f45a2d805ea0)



![image](https://github.com/Reshmarathod/Bing-News-End-to-End-Microsoft-Azure-Fabric-Data-Engineering-Project-Pyspark/assets/146751905/5af9b0ba-58c1-4201-b312-9ce2ab7786af)




### 6.Automation with Data Activator

Implemented an email trigger using the Data Activator tool to send emails to users whenever positive news 
 articles are received. Data Activator enables automation of data-driven actions based on predefined criteria, 
enhancing operational efficiency and proactive decision-making.



 <img width="660" alt="image" src="https://github.com/Reshmarathod/Bing-News-End-to-End-Microsoft-Azure-Fabric-Data-Engineering-Project-Pyspark/assets/146751905/70d2621a-79cc-4887-b45d-b3ba10dbff41">




Through the integration of Microsoft Azure and Fabric technologies, this project demonstrates a comprehensive 
approach to data engineering and analytics, from ingestion to visualization and automation. By leveraging 
services such as Data Factory, Fabric Notebooks, Synapse Analytics, and Power BI, organizations can effectively 
harness the power of their data to drive informed decisions and achieve strategic objectives.












