# Introdcution to Data Engineering

## Modern Data Ecosystem and Role of Data Engineering

The value we derive from data depends on:

- Accuracy of data
- Accessibility of data when we need it

A modern data ecosystem includes whole network of **interconnected**, **independent** and **continually evolving** entities.

It involves:

- Data integrated from disparate sources.
- Different types of analysis and skills to generate insights.
- Active stakeholders to collaborate and act on insights generated.
- Tools, applications and infrastructure to store, process and disseminate data as required.

**Data sources**:

- Structured
- Unstructured

When working with many data sources,

- The first step is to pull a copy of data from the original sources into a data repository. At this stage, we look at only
  - Acquiring the data we need
  - Working with data formats, sources and interfaces through which data can be pulled.
  - *Challenges*: reliability, security and integrity of the data.
- Once the data is in common place(Enterprice data repository)
  - Raw data needs to be organized, cleaned up, optimized for access
  - Conform to compliances and standards enforced in the organization.
  - *Challenges*: Data management, repositories that provide high availability, flexibiliy, accessibiliy and security.
- Finally, Business stakeholders, Applications, programmers, analysts, data science use cases all pulling the data from Enterprice data repository.
  - *Challenges*: Interfaces, APIs, Applications that can get this data to the end users in line with their specific needs.

**Emerging technologies** shaping the modern data ecosystem:

- Cloud technologies
- Machine Learning
- Big Data

### Key Players in the Data Ecosystem

**Data Professionals**

- Data Engineers
  - Develop and maintain data architectures
  - Make data available for business operations and analysis
  - Extract, integrate and organize data from disparate sources
  - Clean, transform and prepare data
  - Design, store and managed data in data repositories
  - Skills:
    - Good knowledge of programming
    - Sound knowledge of systems and technology architectures
    - In-depth understanding of relational databases and non-relational data stores
- Data Analysts
  - Translates data and numbers into plain language for organizations to make decisions.
  - Inspect and clean data for deriving insights
  - Identify correlations, find patterns and apply statistical methods to analyze and mine data.
  - Visualize data to interpret and present the findings of data analysis.
  - Skills:
    - Good knowledge of spreadsheets, writing queries and using statistical tools to create charts and dashboards
    - Programming skills
    - Strong analytical and story-telling skills
- Data Scientists
  - Analyze data for actionable insights
  - Create predictive models using ML and DL
  - Skills
    - Knowledge of Mathematics and Statistics
    - Understanding of programming languages, databases and building data models
    - Domain knowledge
- Business Analysts
  - Leverage the work of Data analysts and Data scientists to look at possible implications for their business and the actions they need to take or recommend.
- Business Intelligence Analysts
  - Do the same work as Business Analysts but focus on market forces and external influences that shape their business
  - Organize and monitor data on different business functions
  - Explore data to extract insight and actionables that improve business performance.
  
**Summary**

- Data Engineers convert raw data into usable data
- Data Analysts use this data to generate insights
- Data scientists use Data analytics and Data Engineering to predict the future using data from the past.
- Business analysts and Business Intelligence analysts use these insights and predictions to drive decisions that benefit and grow their business

### Data Engineering

The field of Data Engineering concerns itself with the mechanics for the flow and access of data

- Provides a robust and scalable structure to make quality data available for decision-making
- Includes the tools and technolgies involved in data manipulation
- Involves understanding the compexities of data and how it is leveraged for fact-finding and decision making

It involves:

- Collecting source data
  - Extracting, integrating and organizing data from disparate sources
  - It includes
    - Data acquistion from multiple sources
    - Data architecture for stroing source data
- Processing data
  - Cleaning, transforming and preparing data to make it usable
  - For this we need:
    - Distributed systems for processing data
    - Pipelines for extracting, transforming and loading data into data repositoris
    - Solutions for safeguarding quality, privacy and security of data
    - Performance optimization
    - Adherence to compliance guidelines
- Storing data
  - Storing data for reliability and easy availablity of data
  - For this we need:
    - Data stores for storage of processed data
    - Scalable systems
    - Ensuring data privacy, security, compliance, monitoring, backup and recovery
- Making data available to users securely
  - APIs, sevices and programs for retrieving data for end-users
  - User access through interfaces and dashboards
  - Checks and balances to ensure data security

Data Engineering is a team sport:

- Architect: Architect data management systems for collecting and storing data
- Database experts: Optimize data stores for high availablity
- Proficiency in Data tools, programming languages and distributes dystems

## Responsibilties and Skillsets of a Data Engineer

At broad level, Data Engineers:

- Extract, organize and integrate data from disparate sources
- Prepare data for analysis and reporting by transforming and cleansing it
- Design and manage data pipelines that encompass the journey of data from source to destination systems
- Setup and manage the infrastructure(Data platforms, Data stores, Distributed systems, Data repositories) required for ingestion, processing and storage of data

**Technical Skills**:

- Operating Systems
  - Unix, Linux, Windows Administrative Tools, System Utilities & Commands
- Infrastructure Components
  - Virtual Machines, Networking, Application Services(Load balancing, application performance monitoring), Cloud-based services
- Databases and Data Warehouses
  - RDBMS such as IBM DB2, MySQL, Oracle Database, PostgreSQL
  - NoSQL such as Redis, MongoDB, Cassandra, Neo4J
  - Data Warehouses such as Oracle Exadata, IMB Db2 Warehouse on Cloud, IBM Netezza Performance Server, Amazon Redshift
- Data Pipelines
  - Apache Beam, Airflow, DataFlow
- ETL Tools
  - IBM Infosphere Information Server, AWS Glue and Improvado
- Language
  - Query languages
    - SQL for relational databases and SQL-like query languages for NoSQL databases
  - Programming languages
    - Python, R, Java
  - Shell and Scripting languages
    - Unix/Linux Shell and PowerShell
- Big Data Processing Tools
  - Hadoop, Hive, Spark

**Functional Skills**:

Data Engineering is at the intersection fo Software Engineering and Data Science.

- Ability to convert business requirements into technical specifications.
- Ability to work with complete software development lifecycle which includes Ideation -> Architecture -> Design -> Prototyping -> Testing -> Deployment -> Monitoring
- Understand data's potential application in business
- Understand the risks of poor data management. Covers Data Quality, Data Privacy, Security and Compliance

**Soft Skills**:

Will be working with other roles such as Technical teams, Business users, Analysts, Data Scientists. So, following skill are necessary

- Interpersonal Skills
- Teamwork
- Collaboration
- Effective communication

<hr style="border:2px solid gray">

## Data Engineering Ecosystem

A Data Engineer's ecosystem includes the infrastructure, tools, framkeworks and processes for:

- Extracting data from disparate sources
- Architecting and managing data pipelines for transformation, integration and storage of data
- Architecting and managing data repositories
- Automating and optimizing workflows and flow of data between systems
- Developing applications needed through the data engineering workflow

**Data**:

- Structured
  - Data that follows a rigid format and can be organized into rows and columns.
  - eg: relational databases, spreadsheet
- Semi-structured
  - Mix of data that has consistent characteristics and data that does not conform to a rigid structure
  - eg: Email, Json
- Unstructured
  - Data that is complex and mostly qualitative information that cannot be structured into rows and columns.
  - eg: photo, videos, text file, social media contents

**Data Repositories**:

- Transactional or Online Transaction Processing(OLTP) System
  - Designed to store high volume day-to-day operational data
  - eg: online banking transactions, ATM transactions etc
  - Typically relational, but can also be non-relational
- Analytical or Online Analytical Processing(OLAP) System
  - Optimized for conducting complex data analytics
  - Include reltional and non-relational databases, data warehouses, data marts, data lakes and big data stores.

**Data Integration**:

Collated --> Processed --> Cleansed --> Integrated --> Users

**Data Pipeline**:

A set of tools and processes that cover the entire journey of data from source to destination systems.

**Languages**:

- Query languages
  - For querying and manipulating data
  - eg: SQL
- Programming languages
  - For developing data applications and controlling application behaviour
  - eg: Python, R, Java
- Shell and Scripting languages
  - For repetitive and time-consuming operational tasks
  - eg: Unix/Linux Shell, PowerShell

**BI and reporting Tools**:

- Collect data from multiple data sources and present them in a visual format, such as interactive dashboards.
- Visualize data in real-time and pre-defined schedule

**File formats**:

- Delimited text file formats eg: CSV, TSV
- Microsoft Excel Open .XML spredsheet, or .XLSX
- Extensible Markup Language, or .XML
- Portable Document Format, or. PDF
- JavaScript Object Notation, or .JSON

**Data Sources**:

- Relational Databases
- Flat File and XML datasets
- APIs and Web Services
- Web Scraping
  - Popular web scraping tools: BeautifulSoup, Scrapy, Pandas, Selenium
- Data Streams and Feeds
  - Popular technologies used to process data streams include: Kafka, Apache Spark and Apache Storm
  - RSS(Really Simple Syndication) Feeds: capturing data from online forums and news sites where data is refreshed on an ongoing basis.

**Meta Data**:

Metadata is data that provides information about other data.

Three main types of metadata:

- Technical metadata
  - Defines the data structures in data repositories or platforms, primarily from a technical perspective.
  - eg:
    - Tables that record information about the tables stored in a database
    - A data catalog, which is an inventory of tables that contain information
  - For relational databases, technical metadata is typically stored in specialized tables in the database called the *System Catalog*.
- Process metadata
  - Describes the processes that operate behind business systems such as data warehouses, accounting systems, or customer relationship management tools.
  - Tracking things like:
    - process start and end times
    - disk usage
    - where data was moved from and to
    - how many users access the system at any given time
  - Invaluable for troubleshooting and optimizing workflows and ad hoc queries.
- Business metadata
  - Information about the data described in readily interpretable ways, such as:
    - how the data is acquired
    - what the data is measuring or describing
    - the connection between the data and other data sources
  - Useful for users who want to explore and analyze data. Help them to find data which is meaningful and valuable and know where the data can be accessed from.

Metadata management:

- Creation of a reliable, user-friendly data catalog is the primary objective of a metadata management model.
- A modern metadata managment model will include a web-based user interface that enables users to easily search for and find information on key attributes such as CustomerName or ProductType.
- This kind of model is central to any Data Governance initiative.
- Well managed metadata helps to understand both the business context associated with the enterprise data and the data lineage, which helps to improve data governance.
- **Data lineage** provides information about the origin of the data and how it gets transformed and moved, and thus it facilitates tracing of data errors back to their root cause.
- The key focus areas of **data governance**:
  - include
    - availability
    - usability
    - consistency
    - data integrity
    - data security
  - includes establishing processes to ensure effective data management throughout the enterprise such as accountability for the adverse effects of poor data quality and ensuring that the data which an enterprise has can be used by the entire organization.
- Popular metadata management tools:
  - IBM InfoSphere Information Server
  - CA Erwin Data Modeler
  - Oracle Warehouse Builder
  - SAS Data Integration Server
  - Talend Data Fabric
  - Alation Data Catalog
  - SAP Information Steward
  - Microsoft Azure Data Catalog
  - IBM Watson Knowledge Catalog
  - Oracle Enterprise Metadata Management (OEMM)
  - Adaptive Metadata Manager
  - Unifi Data Catalog
  - data.world
  - Informatica Enterprise Data Catalog

### Data Repositories

Data repositry is a general term used to refer to data that has been collected, organized and isolated for using in business operations as well as business and data analysis.

Types:

- Databases
  - Collection of data for input, storage, search, retrieval and modification of data.
  - DBMS is a set of programs for creating and maintaining the database. Allows to store, modify and extract info from database using queriesd.
  - Types of databases:
    - Relational
    - Non-relational
- Data Warehouses
  - Consolidates data through the ETL process into one comprehensive database for analytics and business intelligence.
- Big Data Stores
  - Distributed computational and storage infrastructure to store, scale and process very large datasets.
  
#### RDBMS

- Collection of data organized into a table structure where the tables can be linked or related based on data common to each.
- Ideal for the optimized storage, retrieval and processing of large volumes of data.
- Relational databases can be:
  - Open-source with internal support
  - Open-source with commercial support
  - Commercial closed-source
  - eg: IBM DB2, MS SQL Server, MySQL, Oracle Database, PostgresSQL
  - Cloud based relational database services
    - eg: Amazon RDS, Google Cloud SQL, IBM DB2 on Cloud, Oracle Cloud, Azure SQL
- Advantages
  - Create meaningful information by joining tables
  - Flexibility to make changes while the database is in use
  - Minimize data redundancy
  - Ease of backup and disaster recovery by offering export and import options.
  - ACID compliant, ensuring accuracy and reliability in database transactions.
- Use cases
  - OLTP
  - Datawarehouse(OLAP)
  - IoT Solutions
- Limitations
  - Does not work well with semi-structured and unstructured data.
  - Entering a value greater than the defined length of a data field results in loss of information

#### NoSQL

- Provides flexibile schemas for the storage and retrieval of data.
- Chosen for their attributes arond scale, performance and ease of use.
- Built for specific data models
- Has flexibile schemas that allow programmers to create and manage modern applications.
- Do not use a traditional row/column/table database desing with fixed schemas.
- Can store structured, semi-structure and unstructured data.
- Based on model being used for storing data, four common types of NoSQL databases:
  - Key-value store
    - Storing data as collection of key-value pairs.
    - **Key**: attribute of data that is a unique identifier.
    - eg: Redis, Memcached, DynamoDB
    - Usecases: user session data, user preferences, real-time recommendations, targeted advertising, in-memory data caching.
  - Document based
    - Store each record and it associated data within a single document.
    - Enable flexibile indexing, powerful adhoc queried and analytics over collection of documents.
    - Usecases: eCommerce platforms, medical records storage, CRM platforms and analytics platforms.
    - eg: MongoDB, DocumentDB, CouchDB, Cloudant
  - Column based
    - Data is stored in cells groupd as columns of data instead of rows.
    - A logical grouping of columns is referred to as a column family.
    - As all cells corresponding to a column are saved as a continuous disk entry, making access and search easier and faster.
    - Use cases: systes that required heavy write requests, storing time-series data, weather data and IoT data.
    - Not good for: running complex queries, change quering pattern frequently.
    - eg: Cassandra, HBase
  - Graph based
    - Use a graphical model to represent and store data.
    - Use for visualizing, analyzing and finding connections between different pieces of data.
    - Good for: social networks, product recommendations, network diagrams, fraud detection, access management.
    - Not god for processing high volumes of transactions
    - eg: Neo4J, CosmosDB

#### Data Warehouses, Data Marts and Data Lakes

**Data Warehouses**:

- Used for storing modelled, structured, analysis ready data
- Has a 3-tier architecture
  - Database Servers(extracting data from different sources)
  - OLAP Server(process and analyze information coming from database servers)
  - Client-Front end layer for quering, reporting and analyzing data
- Benefits of cloud-based data warehouses:
  - Lower costs
  - Limitless storage and compute capabilities
  - Scale on a pay-as-you-go basis
  - Faster disaster recovery
  - eg: teradata, Oracle Exadata, IBM Db2, Netezza, Amazon Redshift, Google BigQuery, Cloudera, Snowflake
  
**Data Marts**:

- Sub-section of the data warehouse.
- Build specifically for a particular business function, purpose or community of users.
- Three types:
  - Dependent
    - Offer analytical capabilities for a restricted area of a Data Warehouse.
    - Provides isolated security and performance
  - Independent
    - Created from sources other than an Enterprise Data Warehouse such as Internal Operational Systems or External Data.
  - Hybrid
    - Combine inputs from Data Warehouses, Operational Systems and External Systems.
- Purpose:
  - Provide relavant data to users on time.
  - Accelerate business processes
  - Provide a cost and time efficient way in which data driven decisions can be taken.
  - Improve end-user response time
  - Provide secure access and control

**Data Lakes**:

- Store large amounts of structured, semi-structured and unstructured data in their native format.
- Data can be loaded without pre-defined structure and schema
- Exists as a repository of raw data straight from the source, to be transformed based on the use case.
- Data is classified, protected and governed.
- A reference architecture that combines multiple technologies.
- Can eb deployed using
  - Cloud Object Storage eg: Amazon S3
  - Large-scale distributed systems such as Apache Hadoop
  - RDBMS or NoSQL data repositories
- Benefits:
  - Ability to store all types of data(unstructured, semi-structured and structured data)
  - Agility to scale based on storage capacity
  - Saving time in defining structures, schemes and transformations as data is imported in original format.
  - Ability to repurpose data in several different ways and use cases.
  - Vendors providing data lakes: Amazon, cloudera, Google, IBM, Informatica, Microsoft, Oracle, SAS, Snowflake, Teradata
