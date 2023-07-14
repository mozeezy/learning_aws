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