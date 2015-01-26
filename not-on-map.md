# Projects not listed on map

## Polybase
### Strengths
 - A MPP/Hadoop/Cloud (PDW/Hadoop/Azure) blend 
 - Split query execution philosophy
 - SQL users agnostic of whether the query executes on Hadoop or PDW
 - Users are also agnostic of underlying OS
 
### Weaknesses
 - Tied to Hadoop for now. May support other engines in the future
 - No plans for integration with SQL Server as Polybase uses a Data Management Service (DMS) native to PDW
 
### References
 - A [brief comparison](http://nosql.mypopescu.com/post/52620986886/main-difference-between-hadapt-and-microsoft) of Polybase wih Hadapt/HAWQ/SQL-H
 - From the above analysis, one can infer that Polybase/SQL-H/HAWQ do not leverage Hadoop/MapReduce's fault-tolerance, scalability and the ability to 
 process unstructured data fully. They, however, enable users to push data operations at the source and perform analysis without migrating data.
 - http://gsl.azurewebsites.net/Projects/Polybase.aspx
 - http://news.microsoft.com/2014/04/15/microsoft-delivers-data-platform-for-the-era-of-ambient-intelligence/
 - http://blogs.technet.com/b/dataplatforminsider/archive/2014/06/02/polybase-in-aps-yet-another-sql-over-hadoop-solution.aspx
 
 
## Cascading Lingual
### Strengths
  - ANSI SQL Compliant
  - JDBC connector for integration with BI tools
  - Integrate data from heterogenous sources ( a Cascading power)
  - Utilizes optiq's cost-based optimizer

### Weaknesses
  - Query engine on Hadoop: No support for other data sources
  - No ODBC connectivity

### References
  - http://www.cascading.org/projects/lingual/


## Spark-SQL
### Strengths
  - Mix and match SQL and more advanced analytics programming APIs
  - Unlike Shark, developed ground-up to leverage underlying SPARK capabilities
  - allows declarative transformations on groups of tuples (partitioned and loaded as SchemaRDDs)
  - Multiple interfaces (Scala/Python/Java/Hive-QL)
  - Multiple programming options (SQL/MLLib/Graphlab/Spark)
  - Multiple data sources(HDFS/S3) and data formats(Hive/Json/Parquet) support
  - Allows integration with BI tools with ODBC/JDBC support
  - Plug and play UDF support to allow registering UDFS
  - No boxing of primitives when evaluating expressions. Extended Scala API for adding this support
  - Operations such as ETL + data manipulation + data query are all performed seamlessly within the same pipeline without intermediate HDFS read/writes
  
### Weaknesses
  - No monitoring tool or API to get a picture of in-memory RDDs


### References
  - [Interesting comparison with Apache Flink](http://www.slideshare.net/KostasTzoumas/apache-flink-api-runtime-and-project-roadmap) that talks about blocked staging in Spark vs pipelined staging in Flink. 
  - http://databricks.com/blog/2014/07/01/shark-spark-sql-hive-on-spark-and-the-future-of-sql-on-spark.html
  - http://www.slideshare.net/jeykottalam/spark-sqlamp-camp2014
  - http://www.slideshare.net/Hadoop_Summit/building-a-unified-data-pipeline-in-apache-spark
  - http://www.cs.berkeley.edu/~matei/papers/2010/hotcloud_spark.pdf
  - https://www.cs.berkeley.edu/~matei/papers/2012/nsdi_spark.pdf
  

 
## Datasalt's Splout SQL
### Strengths
  - Targeted towards web/mobile applications 
  - Partitions and indexes data on Hadoop
  - Real-time querying with pre-computed aggregations

### Weaknesses
  - Read only views for batch processing supported
  - No incremental data support  

### References
  - http://sploutsql.com/philosophy.html



## Apache Phoenix
### Strengths
  - Full SQL support (including DML) on HBase

### Weaknesses
  - For certain usecases, an application needs to control concurrency by specifying timestamps explicitly

### References
  - Interesting tagline "We put the SQL back in NoSQL"
  - http://phoenix.apache.org/
  - http://hortonworks.com/blog/hbase-hive-better-together/


## DrawnToScale's Spire (Now closed)
### Strengths
  - Provided SQL support on top of HBase

### Weaknesses
  - It is not [shutdown](https://gigaom.com/2013/05/17/database-startup-drawn-to-scale-is-closing-down/)

### References
  - https://gigaom.com/2012/07/24/how-one-startup-wants-to-inject-hadoop-into-your-sql/

