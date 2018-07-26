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

# [Data Warehouse Guide](https://panoply.io/data-warehouse-guide/)

 [What are OLTP and OLAP. What is the difference between them?](https://stackoverflow.com/a/33539330/5200896)
 
 [Kimball and Inmon DW Models](https://bennyaustin.wordpress.com/2010/05/02/kimball-and-inmon-dw-models/)
 
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
 
 
### [Difference Between Fact Table and Dimension Table](https://www.guru99.com/fact-table-vs-dimension-table.html)
- [Difference between Fact table and Dimension table?](https://stackoverflow.com/a/20037663/5200896)

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
 
 
 
