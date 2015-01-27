# Microsoft Azure Search
##Strengths:
- Control over index creation to manage Full Text Search. faceted navigation, [auto complete queries and scoring profiles](https://msdn.microsoft.com/library/azure/dn798933.aspx)

##Weaknesses
- Search based only on one index (despite the ability to create multiple indexes)
- All of the indexed data must be persisted within Azure Search.
- [No support for logging, analysis of search results (will have to be implemented by clients sites if required)](
- No mechanism for measuring query throughput 
- limits on storage 
(https://msdn.microsoft.com/library/azure/dn798933.aspx)

##References:
- https://msdn.microsoft.com/library/azure/dn798933.aspx
- https://www.youtube.com/watch?v=cDCA2PfBR-4

# Lucene/solr
##Strengths:
- Industry tested text based search (works with any file whole string content can be extracted)  
- supports [Pluggable Ranking models]( http://www.ibm.com/developerworks/library/j-solr-lucene/)
- supports joins and grouping, distributed and No-Sql features

##Weaknesses
- [Real time Latency, gets bigger with index](https://karussell.wordpress.com/2011/07/13/jetslide-uses-elasticsearch-as-database/
)
- challenged in fuzzy search and geo search
- initially not designed for instant search and forward recommendations (later retrofitted)

##References:
- http://trijug.org/downloads/TriJug-11-07.pdf
- https://karussell.wordpress.com/2011/07/13/jetslide-uses-elasticsearch-as-database/
- http://www.ibm.com/developerworks/library/j-solr-lucene/


# ElasticSearch
##Strengths:
- [Realtime Get, Multitenant and Fuult Tolerant]( http://en.wikipedia.org/wiki/Elasticsearch)

##Weaknesses
- [Lacks Distribution Transactions](https://karussell.wordpress.com/2011/07/13/jetslide-uses-elasticsearch-as-database/)
- [Versioning feature not up to the mark](https://karussell.wordpress.com/2011/07/13/jetslide-uses-elasticsearch-as-database/) 

##References:
- https://karussell.wordpress.com/2011/07/13/jetslide-uses-elasticsearch-as-database/
- http://en.wikipedia.org/wiki/Elasticsearch



# SRCH2
##Strengths:
- In-Memory search engine, incremental caching, encoded two-way index : all resulting in better throughput 
- built ground up in C++, build on different algorithms and design than lucene.. enables better forward search
- designed to address requirements of mobile and non-traditional device applications
(http://srch2.com/srch2-solr-benchmark-4x-throughput-increase/)

##Weaknesses
- limite scope for customization (compared to open source solutions)
- [not embraced extensively](http://db-engines.com/en/ranking/search+engine) 
   may be due to competition from existing and/or big players)

##References:
- http://srch2.com/srch2-solr-benchmark-4x-throughput-increase/
- http://db-engines.com/en/ranking/search+engine



# HP Autonomy
##Strengths:
- based on pattern matching (hence is Language independent)
- Supports data in a multiple file formats (about 1000) including rich media (audio, video etc)
- good at searches driven by queries that include surmised or contextual information
(http://www.autonomy.com/products/idol)

##Weaknesses
- [relies of big hardware]( http://www.enterprisesearchblog.com/exalead/) 
- HP acquisition casts doubts on future search capability due to [product positioning]( http://www.extended-content.com/wp-content/uploads/2013/05/Gartner-Magic-Quadrant-For-Enterprise-Search.pdf
)

##References:
- http://www.autonomy.com/products/idol
- http://www.enterprisesearchblog.com/exalead/
- http://www.enterpriseappstoday.com/crm/marketing-clouds-salesforce-oracle-ibm-battle-it-out.html
- http://www.extended-content.com/wp-content/uploads/2013/05/Gartner-Magic-Quadrant-For-Enterprise-Search.pdf




# Oracle Endeca Server
##Strengths:
- Unique No-Sql like data model and in-memory architecture
- Supports 35 distinct languages
- can handle varied and disparate data sources.

##Weaknesses
- relies on apriori organization of data into its data model
- product positioning post acquisition endangers search capability

##References:
- http://docs.oracle.com/cd/E40521_01/index.htm



# Attivio
##Strengths:
- search + context enrichment (Predictive Analysis)
- Schema-on-read index, no need for data modeling
- directly connects to any source of information
(http://search.attivio.com/)


##Weaknesses
- Limited monitoring of administrative capabilities 
- Federation capabilities lag behind others
(http://www.extended-content.com/wp-content/uploads/2013/05/Gartner-Magic-Quadrant-For-Enterprise-Search.pdf)

##References:
- http://search.attivio.com/
- http://www.extended-content.com/wp-content/uploads/2013/05/Gartner-Magic-Quadrant-For-Enterprise-Search.pdf




# IBM Infosphere Data Explorer

##Strengths:
- format and location agnostic, prebuilt optimization connectors 
- prebuilt framework for indexing from common data repositories and federation option forc search rngine and third party feeds
- real time content delivery 
- support for wide variety of security models

##Weaknesses
- BI capability not as good as competing products (e.g attivio)
(http://blogs.forrester.com/boris_evelson/12-04-25-data_discovery_and_exploration_ibm_acquires_vivisimo)
 
##References:
- http://www.ndm.net/datawarehouse/pdf/ibm/IBM-InfoSphere-Data-Explorer-Vivisimo.pdf
- http://blogs.forrester.com/boris_evelson/12-04-25-data_discovery_and_exploration_ibm_acquires_vivisimo



# Lucidworks
##Strengths:
- based on Solr, open source model encourages try before buying
- Advances signal processing, extensible connector framework 	

##Weaknesses
- Lags behind others in Federation options
- understanding results difficult 
- No apps or widgets for mobile use 
(http://www.extended-content.com/wp-content/uploads/2013/05/Gartner-Magic-Quadrant-For-Enterprise-Search.pdf)

##References:
- https://docs.lucidworks.com/display/fusion/Lucidworks+Fusion+Documentation
- http://www.extended-content.com/wp-content/uploads/2013/05/Gartner-Magic-Quadrant-For-Enterprise-Search.pdf



# Marklogic
##Strengths:
- Enterprise NoSQL database with rich database features (ACID, HA, Security)
- on premise or cloud deployable 
- proven and strong query & search capability
- Advances signal processing, extensible connector framework 	

##Weaknesses
- Lags behind others in Federation options
- No apps for mobile use 
(http://www.extended-content.com/wp-content/uploads/2013/05/Gartner-Magic-Quadrant-For-Enterprise-Search.pdf)

##References:
- http://www.marklogic.com/
- http://www.extended-content.com/wp-content/uploads/2013/05/Gartner-Magic-Quadrant-For-Enterprise-Search.pdf



# Splunk
##Strengths:
- powerful search, analysis and visualization
- collects and indexes machine data from any source
- on premise, cloud and hybrid deployable
	
##Weaknesses
- Lags behind others in Federation options
- complex set-up process and expensive (for log analysis capability only)
- users needs to learn proprietary query language
(http://www.hoardinginformation.com/6-reasons-why-splunk-might-be-bad-for-you/)

##References:
- http://www.splunk.com/en_us/products/splunk-enterprise.html
- http://www.slant.co/topics/326/compare/~splunk-all-in-one_vs_logstash-all-in-one_vs_logentries-all-in-one
- http://www.hoardinginformation.com/6-reasons-why-splunk-might-be-bad-for-you/




# Logentries
##Strengths:
- supports multiple formats, sources and wide range of platforms (including mobiles) 
- open API, unlimited centralized log data storage and real time visibility of log analysis
	
##Weaknesses
- ??

##References:
- https://logentries.com/
- http://www.slant.co/topics/326/compare/~splunk-all-in-one_vs_logstash-all-in-one_vs_logentries-all-in-one



# Loggly
##Strengths:
- centralized log data storage and real time visibility of log analysis
- Agent free set-up
- supports any text based logs across a range of sources (including routers, switches) 

	
##Weaknesses
- ??

##References:
- https://www.loggly.com/



# SumoLogic
##Strengths:
- supports multiple formats and wide range of data sources 
- centralized log data storage and real time visibility of log analysis
- transaction analytics
- prediction capability with anomaly detection
	
##Weaknesses
- requires local or hosted collector agent

##References:
- http://www.sumologic.com/



# TIBCO Loglogic
##Strengths:
- supports multiple formats and wide range of data sources 
- strong visualization with in-memory data engine, data mashups and contextual collaboration
	
##Weaknesses
- SIEM functionality not as developed as other vendors

##References:
- http://www.tibco.com/products/event-processing/loglogic-for-machine-data/machine-data-management?capabilities

