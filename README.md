The Scope of the Project :

This is a capstone project for  Data enginerring course where there needs to be an implementaion for Data enginerring concepts learned as part of the Course.
The Following concepts and technologies haven been explored as part of the course :

        1. Data Warehousing using Cassnadra and AWS redshift.
        2. ETL/Data ingestion using Apache Spark
        3. Workflow Automation using Apache Airflow.
        
As the part of this project the data which will be explored is from https://www.kaggle.com/arjunprasadsarkhel/indian-time-use-survey?select=TimeUse-India.csv.
This data has information regarding various activities performed in the Indian households on different states/districts.

There are 3 parts of this data as following:

        1. Acitivity Codes - which describes the Acitivity
        2. Different Indian states.
        3. The collection of data regarding who are the households and what are the activities being performed and also informations like
            which state they belong,duration etc. 
            
The following process will be performed as part of this data analysis:
        1. Data will be read from Amazon s3 using spark read. 
        2. Using Spark DataFrames the data will be manipulated to get the required output as Fact and Dimension tables.
        3. Manipulated data will be stored into the s3 as Parquet format to read further for analysis.

Data Model :

Activity :

    Code : int
    Description : String

State :

    Code : int
    Name : String

TimeUse:

     Id : int
     Key_membno : long
     Key_hhold :  long
     State_Code : int
     District_Code :  int
     district_class : string(Rural,Urban,rural+urban)
     Age : int
     Type_Of_day :  normal, weekly variant and abnormal
     hour_from : int
     hour_to : int
     multiple_activity: bool
     time_spent : int
     withinoroutsidehouse : int (1-inside,2-outside)
     activity_code : int
     mode_of_payment:int
     
 The following analysis can be done on this data :
 
        1. Which is the most popular activity among the housholds.
        2. What is the maximum duration taking for any activity.
        3. Which state has the major activity that is based on Farming. So that banks can help in funding the Farming.
 
 There are much more analysis that can be done on this data to understand further on how actually Indians spent their and what best actions cane be taken to 
 make them productive.
 
     
