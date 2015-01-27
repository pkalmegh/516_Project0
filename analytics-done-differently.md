# SQream
##Strengths:
- Claimed first venture into MPP based analytics on GPUs
- Upto 100x faster results for even real-time insights (high-velocity) data: In verbatim, 
["analyze 18 billion anonymized call data records on a single GPU accelerator"](http://www.geektime.com/2014/03/27/sqream-tech-unveils-new-big-data-platform/)

##Weaknesses
- Relatively new company (founded 2010) with very small footprint (<25 employees)

##References:
- http://sqream.com/

# Rainstor
##Strengths:
- Very high [data ingestion](https://gigaom.com/2012/10/04/rainstor-raises-12m-to-turn-your-big-data-small/) speeds ~1M recs/sec
- [Reduce data storage volume by over 95%](http://en.wikipedia.org/wiki/RainStor) using compression (~40:1) and de-duplication techniques
- Row/Columnar hybrid repository

##Weaknesses
- Focuses only on historical data that need not change over time

##References:
- http://rainstor.com/nstor-awarded-u-s-patents-for-database-archiving-and-schema-evolution/
- Good slides on Reduce Retain Retrieve philosophy of Rainstor 


# MammothDB
##Strengths:
- Lets you interface your SQL reporting tools like Tableau, Cognos, Excel etc to query interactively over Hadoop data
- Star and Snowflake schema compliant. 

##Weaknesses
- Does not look like an actively supported database. Even the blogs are 1-2yrs old. 

##References:
- A good overview of [pricing comparison](http://www.mammothdb.com/mdbsnapshot/) against popular databases
