# [Data Warehouse Guide](https://panoply.io/data-warehouse-guide/)

### SQL DW is not a good match for the following scenarios:

- OLTP workload
- High volume of small reads and writes
- Multi-Tenancy Database
- Frequent changing of schema
- Row by row processing
- JSON, XML data and Spatial, Struct, Array and Map data types
- Power BI direct query requiring dashboard performance
- High concurrency of queries (eg. hundreds of thousands of concurrent queries)
- Small datasets (less than 250GB)
- Disaster recovery with stringent RPO and RTO

### Data Warehouse Infrastructure and Technology

 - Traditional on-premise ETL tools such as **Informatica** and **Ab Initio**.
 - Open source ETL tools such as **Talend**, **Apache Camel** and **Apatar**.
 - Stream processing tools, which allow real-time streaming and transformation of data, such as **Apache Kafka** and **Apache Samza**.
 - Cloud-based ETL services such **Segment**, **Stitch** and **Blendo**.

### Data Lake vs. Data Warehouse
Organizations use data warehouses and data lakes to store, manage and analyze data:

 - **Data warehouses** store structured data, cleaned up and organized for specific business purposes, and serve it to reporting or BI tools used by analysts and business users.
 - **Data lakes** are a newer technology that stores both structured and unstructured data in its original form, and processes it later on-demand.

 [What are OLTP and OLAP. What is the difference between them?](https://stackoverflow.com/a/33539330/5200896)
 
 [Kimball and Inmon DW Models](https://bennyaustin.wordpress.com/2010/05/02/kimball-and-inmon-dw-models/)
 
 ### Traditional Data Warehouse Concepts
 - **Dimension:** Categorizes and provides context for facts and measures, enabling analysis.
 - **Conceptual model:** Defines high-level data entities and relationships between them.
 - **Logical model:** Describes data relationships, entities and attributes in as much detail as possible, without details of implementation.
 - **Physical model:** Represents how to implement data design in a specific database system.
 - **Fact table:** A table consisting of “facts”, metrics or measurements, for a business process and their related dimensions.
 - **Dimension table:** Describes dimensions using dimension keys, values and attributes.
 - **Data warehouse schema:** Defines the structure of the data warehouse—how fact tables are split into dimension tables
 
 - **Inmon approach:** Bill Inmon introduced a top-down approach, which sees the data warehouse as the centralized data repository for the entire enterprise.
 - **Enterprise Data Warehouse:** Consolidates data from across the entire enterprise (as advocated by Inmon).
 - **Kimball approach:** Ralph Kimball described a data warehouse as several separate, specialized data marts, created for the use of different departments.
 - **Data Mart:** a mini-data-warehouse focusing on a specific business subject (as advocated by Kimball).

 - **OLTP:** Online transaction processing systems—fast production databases which typically feed data into the data warehouse.
 - **OLAP:** Online analytical processing systems that analyze historical transaction data using read-only queries and aggregations.
Learn more in the Data Warehouse and OLAP section below.

 - **ETL:** Ingests data into the data warehouse by extracting it from source, transforming and optimizing it for analysis, and loading in batches to the data warehouse.
 - **ELT:** A variation on ETL that extracts raw data, including unstructured data, loads it into the data warehouse, and then transforms the data as required for analysis.
 
 ### Creating a Data Warehouse
 
 - Identify the measure that the organization requires reporting
   - Total Sales
   - Total Costs
   - Total Profit
 - Identify how the measure need to be sliced
   - By Date
   - By Department
   - By Employee
 - Identify where the data lives
   - SQL Server
   - XML
   - Oracle
 - Identify where the data needs to be transformed
   - Insure consistency
   - Aggregations
   - Look ups
   
### Data Modeling
 - Identify the organizations reporting metrics
   - Tipically numeric metrics used by an organization to identify success or failure in specific areas
     - Total Sales
     - Total Costs
 - Identify how these metrics are analyzed
   - By Employee
   - By Department
   - By Customer
   - By Product
   
### [Date Wharehouse Schemas](https://blogs.sap.com/2014/07/05/star-schema-vs-snowflake-schema-vs-fact-constellation-schema/)
- Star Schema
- Snowflake Schema
- Fact Constellation

### Data Modeling Considerations 
- Measures
  - **Additive** - Measures that can be aggregated across all dimensions
    - Quantity
    - Cost
  - **NonAdditive** - Measure that can not be aggregated accros all dimensions
    - Margin
  - **SemiAdditive** - Measures that can be aggreagated across most, but not all dimensions
    - Account balance
    
- Keys
  - Both dimensions and fact tables will contain keys
    - Surrogate key - A primary key that is different than that of the source piramry key
    - Business key - The primary key that is taken from the source
    - Fact tables require compound keys

- **Conformed Dimenison**
  - Dimension that can be used across multiple Fact Tables
  - Used when all business users have the same definations for the dimension
  
- **Non-conformed dimension**
  - Dimension table targeted to a sigle fact table
  - Used when dimensions have different definations for different business units

- **Degenerate Dimension**
  - Dimension information that is contained in the Fact table
    - Policy cancelled
  - Dimension value is stored directly in the fact table
  - No coressponding dimension table
  
- **Shared dimension**
  - Used by multiple facts
  - Dimension key is stored in the fact table
  - Dimension value is stored in the dimension table with other attributes of that dimension
  
### [Slowly Changing Dimensions](http://www.oracle.com/webfolder/technetwork/tutorials/obe/db/10g/r2/owb/owb10gr2_gs/owb/lesson3/slowlychangingdimensions.htm)
- There are three types of SCD
  - Overwrite the old value with the new value
    - Historic infromations is lost
  - Record the new value and maintain the old value
    - Show a to and form date or current and expired
  - A new Columns is created as the attribute changes


 
### Logical Model 
> Describes data relationships, entities and attributes in as much detail as possible, without details of implementation.

- **Dimesion Tables** - Describes dimensions using dimension keys, values and attributes
  - Defined with all:
    - Attributes - Columns
    - Keys - Surrogate and buisness key
    - Data types
- **Fact tables** - A table consisting of “facts”, metrics or measurements, for a business process and their related dimensions
  - Defined with all
    - Measures - Columns
    - Keys - Mapped to the dimensions
    - Data types
    - Additive, NonAdditive or SemiAdditive
    
### Phisical Model 
> Represents how to implement data design in a specific database system.

How the logical model will be stored on the physical resources:
 - Tables
   - Will partitioning be used
   - How many disks are available
   - How many filegroups will be used
 - Log files
   - Should utilize spearate disks
 - RAID considerations

### Indexing
 - **Dimesnion**
  - Insure that nonclustered indexes are created on frequently searched columns
  - Clustered index on the buisness keys
  - NonClustered primary key on the surrogate key
 - **Fct**
   - NonCLustered index on frequently queried columns
   - Clustered index on time dimension key
     - There is the possibility that multiple time dimension keys will exist in which case evaluate the most used for the cluseterd index
     
### Compression
- Row compression
  - Fixed length columns are stored as variable length columns
- Page compression
  - Single instance of redundant data is stored on a single  8kb data page
- Reduce bothspace used and disk IO


# Posts:

- [Difference Between Fact Table and Dimension Table](https://www.guru99.com/fact-table-vs-dimension-table.html)
- [Difference between Fact table and Dimension table?](https://stackoverflow.com/a/20037663/5200896)
- [Defining a Data Warehouse Update Schedule](http://support.pb.com/help/spectrum/9.0/webhelp/en/EnterpriseDataIntegration/EnterpriseDataIntegration/source/SchedulingPopulation/PlanningPopulationSchedule.html)
- [Azure SQL Data Warehouse Workload Patterns and Anti-Patterns](https://blogs.msdn.microsoft.com/sqlcat/2017/09/05/azure-sql-data-warehouse-workload-patterns-and-anti-patterns/)
- [Best practices for loading data into Azure SQL Data Warehouse](https://docs.microsoft.com/en-us/azure/sql-data-warehouse/guidance-for-loading-data)
- [Best practices for Azure SQL Data Warehouse](https://docs.microsoft.com/en-us/azure/sql-data-warehouse/sql-data-warehouse-best-practices#reduce-cost-with-pause-and-scale)
- [Common ISV application patterns using Azure SQL Data Warehouse
](https://blogs.msdn.microsoft.com/sqlcat/2017/09/05/common-isv-application-patterns-using-azure-sql-data-warehouse/)
- [Designing tables in Azure SQL Data Warehouse](https://docs.microsoft.com/en-us/azure/sql-data-warehouse/sql-data-warehouse-tables-overview)
- [Data Warehouse vs. OLAP Cube?](https://stackoverflow.com/a/18923809/5200896)
- [Comparison of Master Data Services Functionality in Web Interface versus Excel Add-In](https://www.sqlchick.com/entries/2013/2/2/comparison-of-master-data-services-functionality-in-web-inte.html)
- [Importing Data Into Master Data Services 2012](https://melissa-coates.squarespace.com/entries/2013/2/16/importing-data-into-master-data-services-2012-part-1.html)
- [Практическое применение Master Data Services в MS SQL Server 2012](https://habr.com/post/224981/)
- [7 ошибок ETL-разработчика](https://habr.com/post/273243/)
- [Create First Data WareHouse](https://www.codeproject.com/Articles/652108/Create-First-Data-WareHouse)
- [Master Data Management - What, Why, How & Who](https://www.profisee.com/master-data-management-what-why-how-who)
- [4 Common Master Data Management Implementation Styles](https://blog.stibosystems.com/4-common-master-data-management-implementation-styles)
- **[Data Integration Solutions for Master Data Management](https://technet.microsoft.com/en-us/library/aa964123(v=sql.90).aspx)**
- [Data Warehouse Surrogate Key Design – Advantages and Disadvantages](http://dwgeek.com/data-warehouse-surrogate-key-design-advantages-disadvantages.html/)
- **[SDC](https://en.wikipedia.org/wiki/Slowly_changing_dimension)**
  - [UNDERSTAND SLOWLY CHANGING DIMENSION (SCD) WITH AN EXAMPLE IN SSIS](http://www.learnmsbitutorials.net/slowly-changing-dimensions-ssis.php)
  - [Slowly Changing Dimensions (SCD) in Data Warehouse](http://dwgeek.com/slowly-changing-dimensions-scd.html/)
  - [Member Revision History in Master Data Services 2016 - Part 1](https://www.mssqltips.com/sqlservertip/4324/member-revision-history-in-master-data-services-2016--part-1/)
  - [MDS and SCD](https://social.msdn.microsoft.com/Forums/sqlserver/en-US/0e941c1f-5ed3-426a-8370-e20bba6a5d04/mds-and-scd?forum=sqlmds)

# Blogs:
- [Data Qualtity Services (DQS)](https://blogs.msdn.microsoft.com/dqs/)
- [MDM/MDS - Jeremy Kashel's Blog](http://blogs.adatis.co.uk/jeremykashel)
- [DWGEEK.COM](http://dwgeek.com/category/dwh/)
- [mssqltips.com](https://www.mssqltips.com/sql-server-tip-category/17/integration-services-development/)

## Definations:

### Model
 - Container of logically related entities
 - Coarsest grain for security settings and deployment
 - Unit of data versioning
 - Boundary for entity relationships
 - Typically named for their "primary" entity
 - 1-N models per MDS instance
 
 RDBMS methaphor: **database**
 
 SSAS metaphor: **cube**
 
 ### Entity
  - Container for master data ("members")
  - Iddentifies the attribute for entity members
  - can be related to each other (1:1, 1:M, N:M)
  - Examples: Product, Customer, Country
  - 1-N entites per moderl
  
 RDBMS metaphor: **table**
 
 SSAS metaphor: **dimension**
 
 ### Entity member 
  - An instance of an entity
  - Defines the attribute values for the instance
  - Example:
    "BK-M18B-40", "Mountain-500 Black, 40", "Black"
  - 1-N members per entity
  
  RDBMS metaphor: **record**
  
  SSAS metaphor: **dimension member**
  
  ### Attribute
   - A data value associated with an entity member
   - May be text, numeric, datetime, link, file
   - May be sourcedd from another entity ("domain based attribute")
     -  RDBMS metaphor: **foreign key**
     - SSAS metaphor: **attribute relationship**
   - Examples: Name, Size, Color, Width, Height
   - 1-N attributes per entity
   
 RDBMS metaphor: **column**
 
 SSAS metaphor: **attribute**
 
 ### Hierarchy
  - A relational arrangement of entity members
  - Types:
   - Derived: based on attributes
   - Explicit: each member can have one parent assigned per hierarchy
     - Mandatory: all mebers must be present
   - Combination: exploicit at the top of aderived hierarchy
   - 1-N hierarchies per model
   
 RDBMS metaphor: **parent/child, hierarchiyd**
 
 SSAS metaphor: **hierarchy**
 
 # Backup & Recovery 

 - [Algorithms for Recovery and Isolation Exploiting Semantics](https://en.wikipedia.org/wiki/Algorithms_for_Recovery_and_Isolation_Exploiting_Semantics)
 
 ### Recovery Models
 - Simple (Full Backup)
 - Full (All backups)
 - Bulk-logged (Full, Differential backup)
 
 ### Backup Typs
 - Full 
 - Differential
 - Transaction log 
 
 - File backups
 - Filegroup backups
 - Partial backups
 - Copy-Only backups
 - Mirror backups
  
 ### Posts
 - [Difference between Full backup and Copy-only full backup](https://dba.stackexchange.com/questions/45876/difference-between-full-backup-and-copy-only-full-backup)
 - [Understanding SQL Server Log Sequence Numbers for Backups](https://www.mssqltips.com/sqlservertip/3209/understanding-sql-server-log-sequence-numbers-for-backups/)
 - [Understanding SQL Server Backup Types](https://www.sqlshack.com/understanding-sql-server-backup-types/)
 - [Understanding SQL Server Recovery Models](https://www.red-gate.com/simple-talk/databases/sql-server/database-administration-sql-server/understanding-sql-server-recovery-models/)
 - [Accelerated database recovery](https://docs.microsoft.com/en-us/sql/relational-databases/accelerated-database-recovery-concepts?view=sql-server-ver15)
 - [Accelerated Database Recovery in Azure SQL](https://docs.microsoft.com/en-us/azure/azure-sql/accelerated-database-recovery)
 - [Accelerated Database Recovery in SQL Server 2019](https://www.mssqltips.com/sqlservertip/5971/accelerated-database-recovery-in-sql-server-2019/)
 - [The Transaction Log (SQL Server)](https://docs.microsoft.com/en-us/sql/relational-databases/logs/the-transaction-log-sql-server?view=sql-server-ver15)
 - [Database Checkpoints (SQL Server)](https://docs.microsoft.com/en-us/sql/relational-databases/logs/database-checkpoints-sql-server?view=sql-server-ver15)
 
 
 # [SSIS Design Patterns](https://social.technet.microsoft.com/wiki/contents/articles/10844.ssis-design-patterns.aspx)
 - [Evaluating 3 Different ETL Workflows](https://www.bbdevnetwork.com/blogs/evaluating-3-different-etl-workflows/)
 - [What is Truncate & Load in ETL](http://wisdomschema.com/2015/08/what-is-truncate-load-in-etl/)
 
 # Tutorials
 - [Database design tutorial](http://en.tekstenuitleg.net/articles/software/database-design-tutorial/intro.html)
 - [SQL Server Integration Services (SSIS) Tutorial](https://www.youtube.com/watch?v=3cPq9FXk-RA&list=PLNIs-AWhQzcmPg_uV2BZi_KRG4LKs6cRs) - youtube
 
 
 # Courses:
 - [Microsoft: DAT251x Introduction to Data Modeling](https://courses.edx.org/courses/course-v1:Microsoft+DAT251x+2T2018/course/)
 - [Microsoft: DAT216x Delivering a Relational Data Warehouse](https://courses.edx.org/courses/course-v1:Microsoft+DAT216x+2T2018/course/)
 - [Microsoft: DAT217x Implementing ETL with SQL Server Integration Services](https://courses.edx.org/courses/course-v1:Microsoft+DAT217x+3T2017a/course/)
 - [Microsoft: DAT226x Creating a Master Data Solution with SQL Server Master Data Services (MDS)](https://courses.edx.org/courses/course-v1:Microsoft+DAT226x+2T2018/course/)
 - [Microsoft: DAT218x Data Cleansing with Data Quality Services (DQS)](https://courses.edx.org/courses/course-v1:Microsoft+DAT218x+2T2018/course/)
