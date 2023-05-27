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
- 
<hr style="border:2px solid gray">

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