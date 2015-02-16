# General References:
- [Comparison of relational database management system](http://en.wikipedia.org/wiki/Comparison_of_relational_database_management_system)
- [BigData Mishmash](http://hadoopecosystemtable.github.io/)

TODO: Categorization based on [IBM Bigdata classification](http://www.ibm.com/developerworks/library/bd-archpatterns1/fig1.png) and [Hadapt's Bigdata Innovators](http://hadapt.com/blog/2012/12/21/classifying-todays-big-data-innovators/) 

# Computation Engines/Frameworks
- Apache Hadoop
- Apache Spark
- Apache Mesos
  - http://radar.oreilly.com/2015/02/a-tale-of-two-clusters-mesos-and-yarn.html

# SQL-on-Hadoop
## Desirable Features:
 - Interactive analytical queries
 - MPP 
 - Complex [Optimized Joins](http://infolab.stanford.edu/~ullman/pub/join-mr.pdf)
 - ANSI SQL compliant
 - Data co-location and Query caching
 - ODBC/JDBC connectivity to support BI tools
 
##References:
- http://www.gruter.com/blog/?p=391
- http://ijltet.org/wp-content/uploads/2013/12/14.pdf
- http://hadapt.com/blog/2013/10/02/classifying-the-sql-on-hadoop-solutions/
- http://www.slideshare.net/DavidPortnoy/hybrid-data-warehouse-hadoop-implementations

##Partnerships/Alliances 
MPP meets Hadoop: These are mostly connector type approaches
 - Oracle Exadata/IBM Netezza with Cloudera
 - MS HD Insight/Teradata with Hortonworks
 - GreenPlum with MapR
 
## PostgreSQL based Analytics on Hadoop:
 - Hadapt
 - Pivotal HAWQ
 - Citus Database
 
## Real time Interactive Analysis
 - Impala
 - Apache Drill
 - JethroData
 
## SQL Layer for HBase
 - Salesforce Phoenix
 - DrawnToScale
 
## ANSI SQL Compliant
 - Cascading Lingual
 - Apache Drill
 - Splice Machine
 
## MPP Architecture
 - Apache Drill
 - Postgres-XL
 - SQream
 
## MPP with Hadoop support
 - Pivotal HAWQ
 - Asterdata SQL-H
 
## Based on Hadoop
 - Hive
 - Impala
 - Giraph
 - Hadapt
 - 
 
## Based on Google Dremel
 - Impala (Google F1)
 - Drill
 - CitusDB
 
 
