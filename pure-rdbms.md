#SQLLite
##Strengths
 - Provides a local data storage (entire DB in single file) as an embeddable library
 - Good for [use-cases](https://www.sqlite.org/whentouse.html) where one needs minimal monitoring and has limited resources (eg. prototyping, temporary setups, web devt)
 - More lightweight on resources than loading data from [certain file formats](https://www.sqlite.org/intern-v-extern-blob.html)
 
##Weaknesses
 - Provides a very basic set of features (ACID, indexes, checkpointing) 
 - [Not a real database] (http://charlesleifer.com/blog/sqlite-small-fast-reliable-choose-any-three-/) (not suitable for client-server, shared resources, highly concurrent DBs, high volumes of data)
 - upto 140TB of database: Very Good for a lightweight DB
 - Allows Fixed table schema and does not enforce column data types
 - Relies on File system security
 
##References: 
 https://www.sqlite.org/about.html
  
#Firebird
##Strengths
 - Multi-Generational Architecture [MGA](http://www.firebirdsql.org/file/documentation/papers_presentations/html/FBFactsheet.html) (diff versions of same record) 
  
##Weaknesses
 - Supports multiple flavors which involves some learning curve [Ref](http://www.linuxjournal.com/article/7010)
 - Embedded version [runs only on Windows](http://stackoverflow.com/questions/222699/which-embedded-database-to-use-in-a-delphi-application)
 
##References:
 Interesting discussion on [likes/dislikes] (http://forums.devshed.com/firebird-sql-development-61/advantages-disadvantages-firebird-sql-106804.html)
  
 
#Actian Ingres
##Strengths
 - A good [hardware scalability ](http://community.actian.com/forum/database-migration/1002-ms-sqlserver-vs-ingres.html)
 - [Low cost of replication](http://community.actian.com/forum/database-migration/1002-ms-sqlserver-vs-ingres.html)
 - Supports [multiple platforms](http://database-management.findthebest-sw.com/l/18/Ingres)
 - Supports [MVCC](http://community.actian.com/forum/comp-databases-ingres/4503-how-different-ingres-2.html). 
 - Geospatial support with latest release
##Weaknesses
 - ODBC driver has access issues
 - Poor logging: Difficult to [find error messages] and events(http://community.actian.com/forum/database-migration/1002-ms-sqlserver-vs-ingres.html)
##References:
 http://www.actian.com/products/operational-databases/ingres/
 
#SAP Sybase ASE
##Strengths
 - Smaller storage costs owing to good compressions
 - Ease of DB administration and maintenance as it is integrated with SAP Portfolio
##Weaknesses
 - Relatively new, so involves high ramp up
##References:
 http://klouddata.com/analytics/database-technology/sap-sybase-ase/key-features-and-benefits/
 
# Postgres-XL
##Strengths
- Suitable for Bigdata applications and multi-tenant environments 
(unlike PostgreSQL and Postgres-XC) 
- Supports MPP parallelism making it suitable for querying over large datasets
- Can be ported as a key-value store
##Weaknesses
- Need to be wary of data locality for better query performance
- Geo-distribution not supported natively but can be made available based on requirements
- No support for automatic failover
##References
- http://www.postgres-xl.org/faq/
- Mozilla Public licencse
- SQL 2008 compliant


# PostgreSQL and MySQL
A very good [discussion](http://www.quora.com/What-are-pros-and-cons-of-PostgreSQL-and-MySQL) on comparing the strengths and weaknesses of the two.
And another [slidedeck here](http://www.slideshare.net/EnterpriseDB/the-great-debate-postgresql-vs-mysql-presentation)

## Notes: 
Although the comparison in the second slidedeck is a bit outdated, most of it still holds good. The first article gives a better and recent picture of what features were lacking before (replication, serializable transactions, etc) which are now part of the PostGres release. To sum it up, MySQL has a better community support (mainly because of multiple storage engine optoins) vs PostgreSQL stands out for its reliability, scalability and performance benefits. 
- https://wiki.postgresql.org/wiki/Why_PostgreSQL_Instead_of_MySQL:_Comparing_Reliability_and_Speed_in_2007
- http://www.wikivs.com/wiki/MySQL_vs_PostgreSQL

## Different flavors of Postgres
- EnterpriseDB ( PostgreSQL, Postgres Plus, Postgres Advanced Server)
- Translattice (PostgreSQL, Postgres-XC, Postgres-XL)

##Different flavors of MySQL
These are binary replacements for MySQL with many more added features. Both Percona and Mariadb [replace the InnoDB](http://serverfault.com/questions/545285/mariadb-cluster-vs-percona-cluster-for-mysql) from MySQL with Percona's XtraDB that uses [Galera](http://galeracluster.com/products/) cluster for replication
- Percona
- MariaDB


#Percona
##Strengths
- Opensource and fully compatible with latest MySQL releases
- Additional benefits of improved security, crash-safe replication, online backup, better monitoring owing to refined profiling and instrumentation
- Cloud support and enables NoSQL computing
##Weaknesses
- Not enough penetrated in the DB community
##References:
- http://www.percona.com/software/percona-server/faq
Good article on [feature comparison](http://www.percona.com/software/percona-server/feature-comparison) of Percona vs MySQL 

#MariaDB and MariaDB Enterprise
##Strengths
- Additional fetures include GIS support, dymanic column support, multi-source replication, multiple storage engines.
##Weaknesses:
- [Limitations](http://blog.secaserver.com/2012/04/mysql-advantages-disadvantages-galera/) caused by the Galera cluster

##References:
- https://mariadb.com/kb/en/mariadb/faq/
- https://mariadb.com/kb/en/mariadb/mariadb-vs-mysql-features/
- https://mariadb.com/kb/en/mariadb/faq/mariadb-vs-mysql-compatibility/

