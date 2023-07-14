### Day07 - Database and Analytics

- Storing data in a database allows for more structure to the data as well as ease of querying into the data.

##### Relational Databases
- A database with tables that have links between them.
- We usually use SQL to perform queries on the data.

##### Non-Relational Databases
- Also known as NoSQL databases
- It has a different model than relational databases
- They store documents, key-value, and graph.
- An example would be JSON-formatted data.
- AWS has an offering to manage databases for us.

##### AWS Relational Database Service (RDS)
- This is a managed database service that uses SQL as a query language.
- Allows us to create databases in the cloud.

##### Amazon Aurora
- This is a relational database engine that supports MySQL and Postgres functionalities.
- This is a proprietary service owned and managed by AWS.

##### RDS Deployments
- Read Replicas: This allows for our RDS database to be replicated so that more users can read from the database.
  - However, writing data is only done to the main RDS database.
- Multi-AZ: This allows for our RDS database to be replicated cross-AZ in the instance of an AZ outage.
  - In this instance, our application RDS database would migrate to the foilover database in a different AZ in the case that there's an AZ outage.
- Multi-Region: This allows to create read replicas in different regions where applications in different regions can read from these replicas. However, writing is done to the main RDS database.
  - This is a good strategy for disaster recovery in the case of a region issue.

##### Amazon ElastiCache
- Allows for in-memory database creation and management. (similar to Redis)
- This reduces the workload from RDS databases in the cases of read-intensive workloads.
- Repeated queries are cached in memory so that our applications can read from the ElastiCache instead of making repeated read/write requests to the RDS database.

##### DynamoDB
- NoSQL database that is highly available with replication across 3 AZ.
- Can scale to handle massive workloads and allows for low-latency data retrieval.
- DynamoDB is a key-value database.

##### DynamoDB Accelator (DAX)
- An in-memory cache for DynamoDB.
- Secure, highly scalable and available.
- This is different than ElastiCache since it's only unique and well-integrated with DynamoDB databases.

##### DynamoDB - Global Tables
- This is a way to make DynamoDB tables accessible across multiple regions with low latency.

##### Redshift
- Based on Postgres and is used for online analytical processing (OLAP).
  - i.e. analyics and data warehousing.
- Loads data once every hour and is 10x better performance than other data warehouses.
- Data is stored in columns (columnar).
- Uses Massively Parallel (MPP) Query Execution to do computations on data.
- It is a pay-as-you-go based on the instances you use.

###### Amazon Elastic Map Reduce (EMR)
- Not a database but helps create Hadoop clusters to be able to process and analyze big data.
  - Hadoop cluster: essentially a collection of computers that are joined by network to perform big data processing by working in parallel with each other.
- Can also be used for machine learning.

##### Amazon Athena
- A fully serverless query that is used to perform analytics against S3 objects.
- Querying is done using the SQL language.
- Ideal for business intelligence, logs, and analytics.

##### Amazon QuickSight
- A serverless business intelligence service that creates dashboards to visualize data.
- Ideal for business analytics, business insights, and building visualizations.
- Integrated with many different database services provided by AWS.

##### DocumentDB
- A NoSQL database which is compatible with MongoDB - which is used to store, query, and index JSON data.
- Fully managed, highly available with replication across 3 different AZ.
- Storage can grow in increments of 10GB up to 64TB.
- Automatically scales to handle heavy workloads.

##### Amazon Neptune
- Fully managed graph database so it is ideal for graph datasets (such as a social network)
- Highly available across 3 different AZ with 15 read replicas.
- Optimized for hard and complex queries.

##### Amazon Quantum Ledger Database (QLDB)
- A ledger is a book which records financial transactions.
- Amazon QLDB stores a company's accounting and financial data.
- Fully managed, serverless, and highly available across 3 different AZ.
- Immutable: no entry can be removed or modified. All entries are encrypted.
- But, you can query into the data using SQL.
- unlike Amazon Managed Blockchain, QLDB has a central component.

##### Amazon Managed Blockchain
- Blockchain: allows for multiple parties to make transactions without the need for a centralized authority.
- This allows to join public blockchain networks or create our own private network.
- Compatible with Hyperledger and Ethereum.

##### Amazon Glue
- Managed extract, transform, and load (ETL) service.
- We use to ETL to prepare and transform data for analytics purpose.
- Fully serverless.
- Glue Data Catalog: a catalog of datasets which can be used by Athena, Redshift, and EMR to build proper schemas.

##### Amazon Database Migration Service (DMS)
- Allows for data migration from one database to the another database.
- Runs on EC2 instances and extracts data from a source DB and inserts it into another DB.
- Supports homogeneous migrations (i.e. Oracle to oracle migrations) and heterogeneous migrations.

##### Summary
- Relational Databases - OLTP: Use RDS and Aurora
- Know the different RDS deployments: Multi-AZ, Read replicas, and Multi-Region.
- In-memory Database: ElastiCache
- Key/Value Database: DynamoDB and DAX (cached)
- Data Warehousing and OLAP: Redshift
- Hadoop Clusters: EMR
- Query data on S3: Athena
- Create dashboards: QuickSight
- MongoDB, JSON, and NoSQL: DocumentDB
- Ledger centralized database: Amazon QLDB
- Ledger decentralized database: Amazon Managed Blockchain
- ETL: Glue
- Database Migrations: DMS
- Graph database: Neptune