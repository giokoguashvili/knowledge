# [SQL Server](https://docs.microsoft.com/en-us/sql/sql-server/sql-server-technical-documentation?view=sql-server-2017)

# Features

- [AlwaysOn](https://www.mssqltips.com/sqlservertip/4717/what-is-sql-server-alwayson/) <br/>
is a marketing term which refers to the high availability and disaster recovery solution introduced when SQL Server 2012 was launched
  - [Failover Cluster Instances (FCI)](https://learn.microsoft.com/en-us/sql/sql-server/failover-clusters/windows/always-on-failover-cluster-instances-sql-server):<br/> 
is a traditional failover clustering solution where all nodes in the cluster have access to the shared storage. In case of a failure, the SQL Server instance fails over to another node in the cluster
  - [Availability Group (AG)](https://learn.microsoft.com/en-us/sql/database-engine/availability-groups/windows/overview-of-always-on-availability-groups-sql-server): <br/>
 is a more advanced HA solution that provides high availability and disaster recovery. It allows you to create a group of databases that can fail over together to another replica (instance)
  - [Contained Availability Group](https://learn.microsoft.com/en-us/sql/database-engine/availability-groups/windows/contained-availability-groups-overview) <br/>
  you can create an availability group without having to create an external cluster or Windows Server Failover Clustering (WSFC) environment
  - [Basic Availability Group (BAG)](https://learn.microsoft.com/en-us/sql/database-engine/availability-groups/windows/basic-availability-groups-always-on-availability-groups?view=sql-server-ver16): <br/>
   replaces the deprecated Database Mirroring feature and provides a similar level of feature support
  - [Distributed Availability Group (DAG)](https://learn.microsoft.com/en-us/sql/database-engine/availability-groups/windows/distributed-availability-groups): <br/>
  A distributed availability group is a special type of availability group that spans two separate availability groups. The availability groups that participate in a distributed availability group don't need to be in the same location. They can be physical, virtual, on-premises, in the public cloud, or anywhere that supports an availability group deployment
  - [Read-Scale Availability Groups without Cluster](https://learn.microsoft.com/en-us/sql/database-engine/availability-groups/windows/read-scale-availability-groups?view=sql-server-ver16#read-scale-availability-groups-without-cluster) <br/>
  secondary replicas were configured for read operations. If high availability wasn't the goal, considerable operational overhead was expended to configure and operate a cluster. SQL Server 2017 introduces read-scale availability groups without a cluster
- Database Mirroring (Depricated)
- Replication
- Log Shipping

- Change Trackong 
- Change Data Capture
- Temporal Tables

- Linked Server



# Services

- [MDS](https://docs.microsoft.com/en-us/sql/master-data-services/master-data-services-overview-mds?view=sql-server-2017) - Master Data Services
- [DQS](https://docs.microsoft.com/en-us/sql/data-quality-services/data-quality-services?view=sql-server-2017) - Data Quality Services
- [SSIS](https://docs.microsoft.com/en-us/sql/integration-services/sql-server-integration-services?view=sql-server-2017) - SQL Server Integration Services
- [SSAS](https://docs.microsoft.com/en-us/sql/analysis-services/analysis-services?view=sql-server-2017) - SQL Server Analysis Services 
- [SSRS](https://docs.microsoft.com/en-us/sql/reporting-services/create-deploy-and-manage-mobile-and-paginated-reports?view=sql-server-2017) - SQL Server Reporting Services


# Termonology
- [RDBMS](https://en.wikipedia.org/wiki/Relational_database_management_system) - Relational DataBase Management System
- [ETL Tools: A Modern List](https://www.alooma.com/blog/etl-tools-modern-list) 
- [OLAP](https://en.wikipedia.org/wiki/Online_analytical_processing) - Online Analytical Processing
- [OLTP](https://en.wikipedia.org/wiki/Online_transaction_processing) - Online Transaction Processing


# Tools
- [SSDT](https://docs.microsoft.com/en-us/sql/ssdt/download-sql-server-data-tools-ssdt?view=sql-server-2017) - SQL Server Data Tools
- [MSDTC](https://blogs.msdn.microsoft.com/florinlazar/2004/03/04/what-is-msdtc-and-why-do-i-need-to-care-about-it/) - Microsoft Distributed Transaction Coordinator
- [CDC](https://docs.microsoft.com/en-us/sql/integration-services/change-data-capture/change-data-capture-ssis?view=sql-server-2017) - Change Data Capture (SSIS)

# [Data Quality Servicves](https://docs.microsoft.com/en-us/sql/data-quality-services/data-quality-services?view=sql-server-2017)
DQS is not an absolute. Provides an assessment of potentially incorrect data based upon semantic model
- Components
 - **Data Cleansing:** Modification, removal or enrichment of data that is incorect or incomplete
 - **Matching:** Identification of semantic duplicates in a rules-vased process
 - **Reference Data Sevices:** Verification of the quality of data using the services of a reference data provider
 - **Profiling:** Analysis of a data source to provide insight inot the qiuality of the data at every stage in the knowledge discovery, domain managment, matching, and data cleansing processes
 - **Monitoring:** Tracking and determination of the state of data quality activities
 - **Knowledge Base:** Data Quality Sevices is a knowledge-driven solution that analyzes data based upon knowledge that you build with DQS
 

 ### Posts
- [SQL Server High Availability and Disaster Recovery Plan](https://www.red-gate.com/simple-talk/databases/sql-server/learn/sql-server-high-availability-and-disaster-recovery-plan/)

### Videos
- [SQL Server High Availability and Disaster Recovery overview](https://www.youtube.com/watch?v=AXGKJAjjWLY)
- [SQL Server Temporal Tables vs Change Data Capture vs Change Tracking - part 3](https://www.mssqltips.com/sqlservertip/5144/sql-server-temporal-tables-vs-change-data-capture-vs-change-tracking-part-3/)
- [Availability Group Readable Secondaries – Just Say No](https://www.sqlskills.com/blogs/jonathan/availability-group-readable-secondaries-just-say-no/)