## Amazon Relational Database Service (Amazon RDS)
- Offers FULLY managed relational database solutions that allows customers to focus on other non-database problems.
- Offers Multi-AZ deployment and automated backups, but you can also manually create backups using DB snapshots.
- Supports different DB engines such as Amazon Aurora, MySQL, PostgreSQL, Microsoft SQL Server, MariaDB, and Oracle Database.
- Multi AZ deployment, and automatically fails over to a standby instance in case of interruptions.
- Flexible pay-as-you-go model.
- Use cases are:
  - Web applications
  - Enterprise workloads
  - Product inventories

 ## Amazon Aurora
 - A <B>managed</b> relational database designed to help reduce unnecessary I/O operations.
- Replicates data across multiple Availability Zones for enhanced durability and fault tolerance.

<b>Aurora offers faster, distributed storage and automatic scaling, while RDS supports a broader range of engines (Oracle, SQL Server) and is often more cost-effective for smaller, predictable workloads.</b>

## NoSQL Databases
- Aka non-relational databases have different structure compared to relational DBs like Amazon RDS. Instead of row and columns, it builds a structure for the data they contain using a key-value pairs instead.
- Some examples of NoSQL DBs are Firebase, and MongoDB.

## Amazon DynamoDB
- A fully managed NoSQL database service that provides fast and predictable performance for both document and key-value data structures. 
- Ideal for applications that require high performance and seamless scaling.
- Scales along with your data without impacting performance. You only pay for the resources that you use, and automatically spreads your data across multiple servers to handle your workload.
- Some examples of practical use cases for DynamoDB are gaming platforms, financial service applications, and mobile applications with global user bases.

## In-memory caches
- High-speed storage layer that temporarily keeps frequently accessed data. This way, it reduces the load on primary databases and speeds up response times for end users.
- When applications need specific information, they first check the cache before requesting it from the original data source.
- Ideal for storing session data, API responses, and database query results.

## Amazon ElastiCache
- Fully managed in-memory caching service that was built to help reduce the complexity of administering in-memory caching systems.
- Automatically detects and replaces failed nodes, which makes it ideal for applications that need consistent high performance.
- High performance for Redis, Valkey, or Memcached instances.

<b>ElastiCache addresses performance bottlenecks by caching frequently accessed data in memory, to reduce the load on primary databases and improve response times.</b>

## Amazon DocumentDB
- A fully managed, MongoDB-compatible service for handling semistructured, JSON-like data with dynamic schemas.
- Perfect for applications requiring frequent schema changes and document-oriented data.

## AWS Backup
- Provides a single dashboard for monitoring and managing backups.
- Eliminates the complexity of managing multiple backup strategies by supporting multiple storage types, such as Amazon Elastic Block Store (Amazon EBS) volumes, Amazon Elastic File System (Amazon EFS) file systems, and various databases.

## Amazon Neptune
- Fully managed, purpose-built GRAPH database service that manages highly connected data sets, like those used in social networking applications.
- Excels at understanding complex relationships that are difficult to identify in traditional relational databases.
- Ideal for relationship mapping and pattern matching applications.
