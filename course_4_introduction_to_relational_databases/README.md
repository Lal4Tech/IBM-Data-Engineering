# Introduction to Relational Databases(RDBMS)

## Relational Database Concepts

### Fundamental Relational Database Concepts

**Information Model vs Data Model**:

- Information model
  - is an abstract, formal, representation of entities that includes their properties, relationships and the operations that can be performed on them.
  - Is at the conceptual level and defines relationships between objects.
  - Types
    - Hierarchical: typically used to show organization charts
- Data Models
  - is defined at more concrete level, are specific and include details.
  - Types
    - Relational Model
      - Most used data model
      - Data is stored in tables
      - Allows for logical and physical data independence and physical storage indepedence

**Entity-Relationship Model(ER Model)**:

- A tool to design relational databases
- Building blocks: Entities, Attributes, relationships between entities

**Relationship**:

Building blocks of a relationship are:

- Entities(represented by rectangle)
- Relationship sets(represented by a diamond with lines connecting asscociated entities)
- Crows foot notations(eg: <, >, |)
- Types
  - One-to-One relationship
    - eg: a book written by one author
  - One-to-Many relationship
    - eg: A book written by many authors
  - Many-to-Many relationship
    - eg: Many authors write many differnt books

**Mapping Entities to Tables**:

- The Entity becomes the table
- The attributes get translated into columns

**Data Types**:

- Information contain in a table column should always be of same type.
- Commonly used data types in RDBMS:
  - Character string
    - Fixed length eg. char(10)
    - Variable length eg. varchar(20)
  - Numeric
    - Integer
    - Decimal
  - Date/time
    - Data
    - Time
    - Timestamp
  - Boolean
  - Binary string
  - Large object
  - XML
  - User defined types(UDT)
- Advantages of using data types
  - Data integrity
  - Data sorting
  - Range selection
  - Data calculation
  - Use of standard function
  
**Relational Model Concepts**:

- Building blocks:
  - Relation
  - Sets
    - A set is a unordered collection of distinct elements
    - Items of same type
    - No order and no duplicates
- Relatinal Database
  - A set of relations
  - Relation is mathematical term for table
  - Made of 2 parts:
    - Relation schema
      - Speficies name of relation, name and type of each column(attribute)
    - Relation Instance
      - a table made up of rows(tuples) and columns(attributes)
  - Degree of relation: is the number of attributes in a relation.
  - Cardinality: number of tuples(rows)

eg: for Relation schema

```sql
AUTHOR(
  Author_ID: char,
  firstname: varchar,
  lastname: varchar,
  email: varchar,
  city: varchar,
  country: char
)      
```

### Introducting Relational Database Products

#### Database Artichitecture

**Deployment Topologies**:

- Local
  - Resides on user's system
  - Single user environment
  - Single-tier architecture
  - Usage scenarios
    - Dev/test
    - Database embedded in a local application
- Cient / Server
  - Database resides on a database server
  - users access database from client systems
  - Typically *2-tier databse architecture*
  - In some scenarios there will be middle-tier(application server laryer) between client and server. Also known as *3-tier architecture*.
- Cloud
  - Database resides in a cloud environment
  - No need to install/maintain software or supporting infrastructure
  - Clients access the database through an application server layer or cloud interface.

<u>2-tier architecture</u>

- Client aplication and remote database server run in seperate tiers.
- Application(C/Java/Python etc) connects to the database through an API or framework.
- Database interface communicates through a database client(Driver(ODBS/JDBC))
- DBMS installed on server has multiple layers
  - Data access layer
    - Includes interfaces for different types of clients such as APIs, CLP(Command Line Processer), Properietary interfaces.
  - Database Enginer layer
    - Compiles queries, retries and processes the data and returns the result set.
  - Database Storage layer
    - Here the data is stored. It can be on the local storeage or on network storage.

<u>3-tier architecture</u>

- Application presentation layer and business logic layer reside in different tiers.
- User interact with a client: presentation layer such as a desktop/mobile application or browser.
- Client application communicates with application server.
  - Application server encapsulate the application and business logic and commjnicate with Database server through a Database API/Driver.

**Distributed Architecture and Clustered Databases**:

- Used for Mission Crtitical / Large scale workloads
- Provides high availability/scalability
- Databases are distributed on a cluster of servers.
- Main types of distributed database architectures:
  1. Shared disk architecture
     - Multiple databse servers share common storage
  2. Shared nothing architecture
     - Replication
       - Changes taking place on a database server are replicated to one or more database replicas.
     - Partitioning
       - Very large tables are split across multiple logical partitions.
     - Shadding: database partitions place on seperate nodes
       - Each shad contains its own compute resource(processing, memory and storage)
       - When clinet issues a query:
         - It's processed in parallel on multipled nodes/shards of database.
         - Query results from different nodes are synthesized and returned to client.

#### Database Usage Patterns

Database Access - Key user roles:

- Data Engineers and Database Administrators: Create/Manage
  - Tools used: Command line, GUI/Web based tools
- Data Scintists and Analysts: Read
  - Tools used by Data scritists: Jupyter, R Studio, Zepplin, SAS, SPSS
  - Tools used by Analysts: Excel, Cognos, PowerBI, Tableau, MicroStrategy
  - SQL Query tools
- Application Developers: Read/Write
  - Programming languages(JS, JavaScript, Python, Ruby etc) uses SQL Interfaces and APIs(JDBS, ODBC, REST APIs etc) to interact with Database.
  - ORM Frameworks(ActiveRecord, Django, .NET Hibernate, Sequelize etc): mask the complexities of the underlying SQL interfaces and APIs.

#### Relational Database Offerrings

**Commercial Relational Databses**:

- Oracle Database
- Microsoft SQL Server
- IBM Db2

**Open Source Relational Databses**:

- MySQL
- PostgreSQL
- SQLite

**Cloud Databases**:

- Amazon DynamoDB
- MS Azure Cosmos DB
- MS Azure SQL DB
- Google BigQuery
- Amazon Redshift

Properties of a  well-designed relational database:

- Accurate
- Easy to access
- Reliable
- Flexible

**Db2**:

- First released in 1983
- Family of products
- Can deploy both on-premises and on cloud
- Features
  - AI Powered functionality:
    - ML algorithms
    - Column store
    - Data skipping
  - Common SQL Engine
  - Support for all data types: structured, semi-structured, unstructured
  - High availability and disater recovery
  - Scalability
  - Table partitioning
- Cloud pak for data includes Db2 and many IBM tools for data

**MySQL**:

- Object relationl DBMS
- Supports relationl and JSON data
- Supports multiple storage engines(component that handles the SQL operations on a table and defines what features that table can use)
  - The default MySQL storage engine is InnoDB which supports
    - Transactions to ensure the consitence of the data.
    - Row-level locking to import mult-user performance
    - Clustered indexes on primary keys to increse perfomance of regularly executed queries
    - Foreign keys to mainatain data integrity.
  - MyISAM storage engine
    - Mainly read operations and few updates
    - For data warehouse and web applications
    - Table-level locking
  - NDB
    - Supports Cluster of mysql servers
    - High availability
    - High redundancy
- Supports High availabilyt and scalability
  - Replication
  - Clustering options
    - InnoDB storge Engine: Primary and multiple Secondary servers
    - NDB Storage engine: MySQL cluster Edition uses this. Multiple server nodes act as data nodes.

**PostgreSQL**:

- Free, Open source, Object-relational DBMS
- Can use all standard relational databse constructs such as keys, transactions, views, functions and stored procedures.
- Can also use some of NoSQL functionality such as JSON for structured data and HSTORE for non-hierarchical data.
- Provides high availability
  - Using two node synchronous replication
- Also support high availability and scalability
  - Using multi-node asynchronous replication
  - One master node distributes its changes to multiple read-only replicas for scalability purpose.
- Commercial editionsl such as EDB PostgreSQL Replication provides multi-master read/write replications.
- Recently added features
  - Partitioning
  - Sharding: enable storing hotizondal partitions on multiple remote servers.

<hr style="border:2px solid gray">


## Using Relational Databases

<hr style="border:2px solid gray">


## MySQl and PostgreSQL

<hr style="border:2px solid gray">

## Project

<hr style="border:2px solid gray">