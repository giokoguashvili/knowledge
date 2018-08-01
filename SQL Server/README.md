# [SQL Server Technologies](https://docs.microsoft.com/en-us/sql/sql-server/sql-server-technical-documentation?view=sql-server-2017)

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
   
### Date Wharehouse Schemas
- Star Schema
- Snowflake Schema

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

# [Data Quality Servicves](https://docs.microsoft.com/en-us/sql/data-quality-services/data-quality-services?view=sql-server-2017)
DQS is not an absolute. Provides an assessment of potentially incorrect data based upon semantic model
- Components
 - **Data Cleansing:** Modification, removal or enrichment of data that is incorect or incomplete
 - **Matching:** Identification of semantic duplicates in a rules-vased process
 - **Reference Data Sevices:** Verification of the quality of data using the services of a reference data provider
 - **Profiling:** Analysis of a data source to provide insight inot the qiuality of the data at every stage in the knowledge discovery, domain managment, matching, and data cleansing processes
 - **Monitoring:** Tracking and determination of the state of data quality activities
 - **Knowledge Base:** Data Quality Sevices is a knowledge-driven solution that analyzes data based upon knowledge that you build with DQS
 
 
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

# Blogs:
- [Data Qualtity Services (DQS)](https://blogs.msdn.microsoft.com/dqs/)

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
 
 
 
