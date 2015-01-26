# Facebook Presto
##Strengths:
- Fast and interactive querying over various data analysis platforms and commercial BI tools
- Effective query monitoring in realtime
- Query over multiple data sources without migrating data

##Weaknesses
- [NOT a database](http://www.slideshare.net/frsyuki/presto-hadoop-conference-japan-2014)
- In verbatim "Query fails if aggregated data doesn't fit in memory" from [here]((http://www.slideshare.net/frsyuki/presto-hadoop-conference-japan-2014))

##References:
- Integration with BI tools achieved using PostgreSQL's ODBC/JDBC drivers: PrestoGres


# Cloudera Impala
##Strengths:
- Moved away from the MapReduce paradigm to support querying over a generic shared-nothing parallel DB (based on Google Dremel)
- Pitching in Parquet columnar file format against the ORC FileFormat from Hortonworks. As seen in below 
[ref](http://pages.cs.wisc.edu/~floratou/SQLOnHadoop.pdf), it clearly outperforms ORC
- Streams data between query stages making it faster than Hive which materializes data between 
stages (or deserializes during scan operations even with the Tez support)
- Forgoes MapReduce's inherent fault-tolerant and dynamic scheduling capabilities. [Ref](http://hadapt.com/blog/2013/10/02/classifying-the-sql-on-hadoop-solutions/)

##Weaknesses
- A complete list of [features not supported](http://www.cloudera.com/content/cloudera/en/documentation/cloudera-impala/latest/topics/impala_faq.html#faq_features_unique_1)
- One of the key things to note is it does not support streaming data, search-based queries, and query checkpointing. 
- No integration with traditional RDBMS 
- Single threaded execution of complex queries involving joins and aggregation slows down performance drastically
- Cannot handle data which exceeds memory size as it does not materialize data between shuffling phase

##References:
- Comparing [Impala vs Hive](http://pages.cs.wisc.edu/~floratou/SQLOnHadoop.pdf)


# JethroData
##Strengths:
- Indexes every column on Hadoop for claimed "fastest" SQL querying on Hadoop
- Generates indexes as data is written into Hadoop
- Supports live streaming and interactive BI with ODBC/JDBC connectivity for almost any BI tool
- Performance depends not on the size of the input dataset but on the size of the resultset

##Weaknesses
- Directly [pitched against Hadapt](http://techcrunch.com/2013/02/27/jethrodata-raises-4-5m-for-new-analytics-database-that-addresses-hadoops-achilles-heel/) making 
- Still in Beta Release (since Jul 2014)

##References:
- http://www.jethrodata.com/home
- Very good [slides](http://www.slideshare.net/ofirm/jethro-data-interactivebionhadoop) comparing JethroData against Impala, Hive, Spark

# EMC-Greenplum Pivotal HD/HAWQ
##Strengths:
- HD: First engine to provide Hadoop Virtualization Extension plug-ins
- HAWQ: Pivotal Xtension Framework (PXF) allows for querying data stored in Hadoop using external tables
- Dynamic pipelining, a combination of Greenplum technologies that enables reuse of queries across Greenplum DWH and Pivotal HD
- Graphlab and MadLib supported
- Cost based optimizer borrowed from Greenplum DB

##Weaknesses
- [Proprietary](http://redmonk.com/sogrady/2013/03/06/pivotal-hd/) ?? (Need to check what does their free offering include)

##References:
- http://www.pivotal.io/sites/default/files/Hawq_WP_042313_FINAL.pdf
- https://thebigdatainstitute.wordpress.com/tag/hawq/
- http://www.slideshare.net/emcacademics/pivotal-hadoop-for-powerful-processing-of-unstructured-data-for-valuable-insights


# Cloudera CDH
##Strengths:
##Weaknesses
##References:
- http://www.experfy.com/blog/cloudera-vs-hortonworks-comparing-hadoop-distributions/

# Apache Tajo
##Strengths:
- Cost based and Progressive query optimizer
- Supports datasets larger than memory

##Weaknesses

##References:
- Gruter providing [Tajo-as-a-service](http://gruter.com/products/taas/)
- Good blog on [What 100x faster actually means](http://www.gruter.com/blog/?p=391)

# Apache Drill
##Strengths:
- Based on Google Dremel/Bigtable, provides SQL-based interface (ANSI SQL compliant) for interactive data analysis
- Nested data exploration supported
- Beyond Hadoop: Also supports NoSQL/RDBMS products
- Forgoes MapReduce's inherent fault-tolerant and dynamic scheduling capabilities. [Ref](http://hadapt.com/blog/2013/10/02/classifying-the-sql-on-hadoop-solutions/)

##Weaknesses
- Many key features like SQL interpreter, storage engines for systems like HBase, Cassandra, etc still in development phase

##References:
- Included in [MapR Release](http://www.infoq.com/news/2014/09/Apache-Drill-MapR-Release)
- http://www.slideshare.net/MapRTechnologies/an-introduction-to-apache-drill-presentation
- https://www.mapr.com/blog/top-10-reasons-using-apache-drill-now-part-mapr-distribution-including-hadoop#.VME0ofnXo8o 

# IBM Big SQL
##Strengths:
- Leverages Hive
- IBM DB2 compatible stored procedure support (like cursors, anon blocks, etc)
- Operations performed in memory with spill over capability enabling support for larger than RAM data 

##Weaknesses
- SQL like; Not SQL compliant
- No optimization, indices (Optimizer based on RDBMS)
- [Rely on user for optimal query writing](http://www.ibm.com/developerworks/library/bd-gobigsql/) to utilize underlying MapReduce paradigm
- Insert rows support is good only for testng purposes as it creates a new file per insertion

##References:
- http://www.slideshare.net/NicolasJMorales/big-sql-30-toronto-meetup-may-2014

# CitusDB
##Strengths:
- PostGreSQL based analytics (carries the benefits of psql)
- Supports NoSQL DBs like MoongoDB
- Based on Google Dremel
- Uses its own execution framework to mitigate MapReduce overheads
- Scheduling policy takes into account the table to blocks mapping info
- ODBC/JDBC compliance

##Weaknesses
- Faces competition from biggies like Impala, Apache Drill, and Google's own query API to BigTable
- Does not provide transactional suuport as PostGreSQL does
- hstore extension that comes with PostGreSQL support needs to be loaded separately

##References:
- http://techcrunch.com/2013/02/20/citus-data-launches-citusdb-an-analytics-database-based-on-google-dremel-with-parallel-processing-at-its-core/
- http://www.citusdata.com/


# Hadapt
##Strengths:
- Execution of queries split between MapReduce and RDBMS engine

##Weaknesses
- Closed source product selling core; no services provided (Hadapt)
- Limited to MapReduce execution engine

##References:
- Polybase has the same query split policy. Not in the list of DBs in the map (http://gsl.azurewebsites.net/Projects/Polybase.aspx)

# SciDB
##Strengths:
- Support SQL querying on multi-dimensional arrays, not tables
- Address issues in complex analytics such as partial results, uncertainty 

##Weaknesses
- Data model geared more towards OLAP science applications; not for OLTP

##References:
- http://www.slideshare.net/sdsc/scidb-open-source-data-management-system-for-dataintensive-scientific-analytics
- http://www.scidb.org/forum/viewtopic.php?f=11&t=1447

# Splice Machine
##Strengths:
- Apache Derby (bringing in ANSI SQL compliance) + HBase/Hadoop (scale-out)
- Real-time analytics with transactional support catering for both OLTP and OLAP workloads
- ODBC/JDBC support

##Weaknesses
- Not a cloud based offering

##References:
- http://www.splicemachine.com/why-splice/differentiators/
- http://www.splicemachine.com/product/how-it-works/

