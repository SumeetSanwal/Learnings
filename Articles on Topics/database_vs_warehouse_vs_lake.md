<h2> DATABASE | DATA WAREHOUSE | DATA LAKE </h2>


| DATABASE                                                                    | DATA WAREHOUSE                                                          | DATA LAKE                                                                                     |
|-----------------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Set of tables related to each other in some sense & using some schema.      | Repo of structured data which has been processed for a defined process. | Massive repo of structured and unstructured data and purpose of this data is not been defined |
| Best for transaction data and OLTP purpose. Used in backedn of applications | Best for analytical processsing.                   ||
| Schema on write - Validate schema when writing                              | Schema on write - Validate schema when writing                          | Schema on read - Structure is imposed when data is read                                       |
| Costly and not used to store lots of historical data.                       | Cost relatively lower than a database                                   | Cost effective for large historic data.                                                       |
| Mysql, Oracle, etc                                                          | Snowflake, Redshift, etc                                                | S3, HDFC, etc                                                                                 |



<h3> OLTP vs OLAP </h3>


|        | OLTP           | OLAP                                                                                                                                                                                 |
|--------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|Stands for|	Online transaction processing	| Online analytical processing                                                                                                                                                         |
|Usage pattern	|Optimized for fast CRUD(create, read, update, delete) of a small number of rows| 	Optimized for running analytical, aggreagtions, etc queries on a large number of rows (aka analytical queries), and ingesting large amounts of data via bulk import or event stream |
|Storage type|	Row oriented| 	Column-oriented                                                                                                                                                                     |
|Data modeling|	Data modeling is based on normalization| 	Data modeling is based on denormalization. Some popular ones are dimensional modeling and data vaults                                                                               |
|Data state|	Represents current state of the data| 	Contains historical events that have already happened  |                                                                                                                             
|Data size|	Gigabytes to Terabytes	| Terabytes and above                                                                                                                                                                  |
|Example database|	MySQL, Postgres, etc| 	Clickhouse, AWS Redshift, Snowflake, GCP Bigquery, etc                                                                                                                              |








<h3> Links </h3>

* Article - [Data Warehouse & Lake](https://www.startdataengineering.com/post/data-lake-warehouse-diff/)
* Article - [Datawarehouse & OLTP vs OLAP](https://www.startdataengineering.com/post/what-is-a-data-warehouse/)
* Youtube - [DATABASE | DATA WAREHOUSE | DATA LAKE](https://www.youtube.com/watch?v=Nn7CFCQLKOs)
* Article - [Data Warehouse & Lake](https://www.qlik.com/us/data-lake/data-lake-vs-data-warehouse)



