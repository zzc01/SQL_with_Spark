# SQL_with_Spark

## Databrick
In this project we use Databrick to write SQL query with Spark. Databrick is a company founded by the creators of Apache Spark [1]. It provides a web platform to run machine learning task at scale using its automated cluster management system. It has a Jupyter notebook like workspace that we can write and run Python, PySpark, SQL, Scala, R codes. We use the community version [2] of Databrick which is free. 

<pre><p align="center">
<img src="https://user-images.githubusercontent.com/86133411/214099576-8a94568a-b370-420c-856b-f008085aafd4.png"  width="600">
</p></pre>

## About the code
In this project we create one database with three tables: members, bookings, facilities. The members table contains the member name, ID, address, join date, etc. 
The facilities table contains the courts name, facility ID, costs, etc. The bookings table has information of the researvations including the member ID, facility ID, reserved time slots, etc. We use Spark to load dataframe save it as a table and utilize SQL to query the database.  
<br/>

### Some useful commands
* PySpark 
  * bookings_df = (spark.read.format(file_type) 
                    .option("inferSchema", infer_schema) 
                    .option("header", first_row_is_header) 
                    .option("sep", delimiter) 
                    .load(file_location_bookings))
  * bookings_df.printSchema()
  * bookings_df.write.format("parquet").saveAsTable(permanent_table_name_bookings)
  * print(spark.version)
  * print(type(spark))
  * print(type(sc))
* SQL 
  * DROP DATABASE IF EXISTS country_club CASCADE
  * CREATE DATABASE country_club
  * SHOW DATABASES
  * USE country_club
  * REFRESH TABLE bookings
  * SHOW tables
  * Subqueries
  * CASE
  * JOIN
  * BETWEEN 

## References 
[1] https://en.wikipedia.org/wiki/Databricks <br>
[2] https://community.cloud.databricks.com/  <br>
