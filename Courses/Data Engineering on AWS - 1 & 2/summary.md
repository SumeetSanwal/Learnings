## Data Lake Architecture
![](../../Images/data_lake_overview_architecture.png)
![](../../Images/data_lake_principles.png)

## Data Pipeline Components
![](../../Images/data_pipeline_components.png)





[//]: # (========================================NEXT MODULE==================================)

## 1. Data Sources
  ![](../../Images/aws_ddb.png)





[//]: # (========================================NEXT MODULE==================================)

## 2. Data Ingestion

  * ### Data Ingestion Considerations
    * Type of Data - Mysql, DDB, ES, etc
    * Data format - structured, un-structured, semi-structured
    * Data Frequency :
      * 1-5 min - Real Time 
      * Less than 1hr - Near Real Time
      * More than 1 hr - Batch
    * Optimal size : 16 - 256mb files to reduce number of I/O operations overhead.
    * Compaction - Clubbing smaller file to make a larger not fragmented file to reduce I/O operations and improve performance.
    * File Format - Parquet, HUDI, ORC, Delta, etc
    * Partitions - Folder structure needed like based on date, cluster, etc partitioning
    * Ingestion Patterns - 
      * Batch Processing - Glue, Spark, AWS sync, COPY to Snowflake, etc
      * Real Time - Kinesis Firehouse, Kinesis Streams, Managed kafka, etc
      * One time on-premise to cloud migration - Data Migration Service(DMS), Snowmobile(hardware device), 
      * Cloud & On-premise Hybrid : Data Connect, Storage Gateway, etc
      
    ![](../../Images/data_ingestion_things_to_focus.png)


  
  * ### Amazon Kinesis 
    
    * ### Type of Kinesis Services?
        ![](../../Images/kinesis_1b.png)

        ![](../../Images/kinesis_2.png)
    <br/>
    <br/>



  * ### Amazon Kinesis Data Stream

    * ### What is Amazon Kinesis Data Streams?
        ![](../../Images/kinesis_1.png)
    <br/>
    
    * ### Kinesis Data Stream Ingestion Architecture
        ![](../../Images/kinesis_3.png)
        ![](../../Images/kinesis_3b.png)
    <br/>
    
    * ### Kinesis Produces
       ![](../../Images/kinesis_4.png)
    <br/>
    
    * ### Kinesis Consumers
       ![](../../Images/kinesis_5.png)
    <br/>
    <br/>



  * ### Amazon Kinesis Firehose

    * ### What is Amazon Kinesis Firehose?
       ![](../../Images/kinesis_firehose_2.png)
    <br/>
       ![](../../Images/kinesis_firehose_3.png)
    <br/>
       ![](../../Images/kinesis_firehose_4.png)
    <br/>
    <br/>
    
    * ### Amazon Kinesis Firehose Architecture
       ![](../../Images/kinesis_firehose_1.png)


    
    

[//]: # (========================================NEXT MODULE==================================)

## 3. Data Storage

  * ### Data Storage Considerations
    ![](../../Images/storage_considerations.png)
  <br/>
  <br/>

  * ### Type of Storage Options in AWS

    * #### Elastic Block Storage {EBS}
      * Two or more AMI can't use the same EBS, so can't be used by multiple AMIs.
      ![](../../Images/ebs.png)

    * #### Elastic File Storage
      * Not as fast as EBS
      * Allows to share drive across several AMIs.
      ![](../../Images/efs.png)
  
    * #### Simple Storage Service {S3}
        * It is a file sharing service which doesn't require an AMI/compute to which it has to be connected to for sharing.
        * Slower than EFS and EBS.
        ![](../../Images/s3.png)



[//]: # (========================================NEXT MODULE==================================)

## 4. Data Catalogue
