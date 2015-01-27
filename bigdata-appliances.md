#Oracle Big Data Appliance
- Capture data using Hadoop and NoSQL databases, use connectors to migrate data and then perform advanced analytics in DWH
- Consists of: 
	- Oracle Exadata 
	- Oracle Exalytics 
	- Hadoop connector (Oracle Data Integrator)
	- Oracle NoSQL DB
	- Oracle R
	- Oracle Linux and Java Hotspot 
	
##Oracle Exadata 

###Strengths:
- Features such as SmartScan for non-indexed table scans are much faster than Oracle Enterprise deployment
- FlashCache for read-intensive environments
- Hybrid columnar compression provide better data optimization

###Weaknesses
- Huge software deployment cost while having a lower hardware appliance cost
- All the new features compel you to lose flexibility For eg. 
	- owing to the FlashCache support, a cache miss incurs a severe overhead 
	- not suitable for random access 
- [Not a good idea to buy this appliance](http://www.pcworld.com/article/2145960/experts-avoid-big-mistakes-with-oracles-exadata.html if all you are looking for is better performance with Oracle)

##References:
- http://www.storage-switzerland.com/articles/Entries/2011/9/8_The_Storage_Challenges_To_Oracle_Exadata.html
- https://451research.com/report-short?entityId=82175&referrer=marketing


## Oracle Exalytics (component of Oracle Big Data Appliance)
###Strengths:
- provides a complete stack: customized hardware/firmware and optimized software 
- In-memory data storage [based on Oracle's timesten](http://www.informationweek.com/software/information-management/oracle-exalytics-is-it-a-must-have-for-bi/d/d-id/1106806?)
- Can be used even if the [data is not stored in Oracle databases](http://www.peakindicators.com/index.php/knowledge-base/111-exalytics-frequently-asked-questions-faq)

###Weaknesses
- [Limitations](http://www.peakindicators.com/index.php/knowledge-base/111-exalytics-frequently-asked-questions-faq) answered in Q11

###References:
- https://www.oracle.com/engineered-systems/exalytics/features.html

# Oracle TimesTen
##Strengths:
- Although it is a in-memory database, it is not required to have the entire database to be loaded. It also supports dymanic loading of Oracle tables
- Allows caching data [while the system is running](http://www.peakindicators.com/index.php/knowledge-base/111-exalytics-frequently-asked-questions-faq)

##Weaknesses
- When deployed out of the Oracle Exalytics or Big Data Appliance, it runs in the application tier
- DB size is limited on a 32-bit architecture

##References:
- http://www.oracle.com/technetwork/database/database-technologies/timesten/faq-091526.html


# IBM Puredata/ IBM Puredata for Operational Analytics 
IBM-Netezza

##Strengths:
- IBM PureData (formerly known as Netezza) is a purpose-built warehousing appliance. 
- Queries require very [less tuning](https://www.linkedin.com/groups/What-are-advantages-disadvantages-Netezza-3998584.S.257759716)
- Most of the processing/optimization done at h/w level making it convenient for users

##Weaknesses
- Not good for OLTP

##References:
- http://www-01.ibm.com/software/data/puredata/analytics/nztechnology/analytics.html

# IBM Informix 
##Strengths:
- Lets you [configure an engine with mem/cpu/disk capacities](http://www.experts-exchange.com/Database/Miscellaneous/Q_11310958.html) and then define databases in the allocated resources
- [Script-based](http://www.123helpme.com/view.asp?id=158444)  web support to include SQL in HTML pages (Datablade)

##Weaknesses
- May have the problem of [Dirty Reads](http://www.experts-exchange.com/Database/Miscellaneous/Q_11310958.html):  when one transaction reads a value that has been rolled back by another transaction

##References:
- http://www-01.ibm.com/software/data/informix/features.html


# Teradata
##Strengths:
- Low latency for interactive data analysis 
- provides a unified view of data from multiple sources 
- Columnar and block level compressions supported

##Weaknesses
- does not cater to very high volumes of raw data (needs cleansed data)
- [Requires specialized hardware](http://infogoal.com/datawarehousing/database.htm) for porting

##References:
- http://blogs.teradata.com/international/tag/enterprise-data-warehouse/


# Teradata Aster
##Strengths:
- Teradata's answer to BigData offering, this platform enables fast interactive analysis on very large volumes of data
- Unified querying with SQL-MapReduce feature which enables end-to-end querying 
- Part of Teradata's unified architecture where it can be integrated with Hadoop data platform

##Weaknesses
- A [smaller customer base](http://info.mapr.com/rs/mapr/images/The_Forrester_Wave_Big_Data_Hadoop_Q12014.pdf) for now

##References:
- http://www.ovum.com/research/teradata-aster-discovery-platform-v5-10/
- http://www.nascio.org/events/sponsors/vrc/Big%20Data%20-%20Teradata%20Unified%20Data%20Architecture%20in%20Action3.pdf


