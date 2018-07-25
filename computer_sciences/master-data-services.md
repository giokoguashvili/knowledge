# [SQL Server Technologies](https://docs.microsoft.com/en-us/sql/sql-server/sql-server-technical-documentation?view=sql-server-2017)

- [MDS](https://docs.microsoft.com/en-us/sql/master-data-services/master-data-services-overview-mds?view=sql-server-2017) - Master Data Services
- [DQS](https://docs.microsoft.com/en-us/sql/data-quality-services/data-quality-services?view=sql-server-2017) - Data Quality Services
- [SSIS](https://docs.microsoft.com/en-us/sql/integration-services/sql-server-integration-services?view=sql-server-2017) - SQL Server Integration Services
- [SSAS](https://docs.microsoft.com/en-us/sql/analysis-services/analysis-services?view=sql-server-2017) - SQL Server Analysis Services 
- [RDBMS](https://en.wikipedia.org/wiki/Relational_database_management_system) - Relational database management system

- [SSDT](https://docs.microsoft.com/en-us/sql/ssdt/download-sql-server-data-tools-ssdt?view=sql-server-2017) - SQL Server Data Tools


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
 
