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


## Apache Flink (previously Stratosphere)
### Strengths
  - Very similar offerings to Apache Spark
  - Provides a in-memory 
  - Multiple programming options (SQL/ML/Graph/Streaming)

### Weaknesses
  - It has not yet penetrated the BigData space in the US. Some say it's Europe's wildcard entry](https://medium.com/chasing-buzzwords/is-apache-flink-europes-wild-card-into-the-big-data-race-a189fcf27c4c) into the Bigdata world
  - Not sure about data format and multiple system support
  - Not a robust ML library
  - Still [working on providing fault-tolerance](http://apache-flink-incubator-user-mailing-list-archive.2336050.n4.nabble.com/Flink-and-Spark-td583.html) for both batch and streaming modes

### References
- http://www.slideshare.net/stephanewen1/apache-flink-overview

