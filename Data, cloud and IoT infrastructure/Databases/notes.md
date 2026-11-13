                    DATABASES
A database is an organized collection of related data stored electronically and managed to allow efficient storage, retrieval, modification, and deletion of information.
A Database Management System (DBMS) is software used to create, manage, access, and control databases.
Examples: MySQL, PostgreSQL, Microsoft SQL Server, Oracle Database, and MongoDB.
  Main functions of a DBMS;
- Data storage and retrieval.
- Data insertion, updating, and deletion.
- Data security and access control.
- Data integrity and consistency.
- Transaction management.
- Backup and recovery.
- Concurrent access management.
- Query processing and optimization.
  Database vs DBMS;
- Database: the organized collection of data.
- DBMS: the software that manages the database.
- Database application: software that interacts with the DBMS to perform specific tasks.
Example: A banking application communicates with a DBMS to retrieve account information and process transactions.

 DATABASE COMPONENTS AND TERMINOLOGY
   Basic relational database terms;
Table: organizes related data into rows and columns.
Row/Record/Tuple: represents one individual entry.
Column/Attribute: represents a particular property of the data.
Field: an individual data value within a record.
Schema: defines the structure of a database, including tables, columns, data types, and relationships.
Instance: the actual data stored in the database at a particular time.
Domain: the set of valid values an attribute can contain.
  Keys;
Keys identify records and establish relationships between tables.
Primary key (PK)
- Uniquely identifies each record.
- Must contain unique, non-null values.
- A table has one primary key constraint, which can consist of multiple columns.
Foreign key (FK)
- References a primary key or another eligible unique key in another or the same table.
- Maintains referential integrity.
Candidate key
- A minimal set of attributes capable of uniquely identifying a record.
Alternate key
- A candidate key not selected as the primary key.
Composite key
- A key consisting of two or more attributes.
Unique key/constraint
- Enforces uniqueness of values in a column or group of columns.
Surrogate key
- An artificial identifier, such as an automatically generated integer or UUID.
  Constraints;
Constraints enforce rules on database data.
- NOT NULL: prevents null values.
- UNIQUE: prevents duplicate values.
- PRIMARY KEY: uniquely identifies records.
- FOREIGN KEY: enforces valid references.
- CHECK: enforces a logical condition.
- DEFAULT: supplies a value when one is not specified.

 TYPES OF DATABASES
  Relational databases (SQL databases);
Store data in tables consisting of rows and columns, with relationships established through keys.
Examples:
- PostgreSQL.
- MySQL.
- Microsoft SQL Server.
- Oracle Database.
- SQLite.
Characteristics:
- Structured schemas.
- SQL query language.
- Referential integrity.
- Transaction support.
- Relationships between tables.
Applications:
- Banking systems.
- Inventory management.
- Student information systems.
- Enterprise applications.
- Financial transactions.
  NoSQL databases;
NoSQL databases support data models that are not restricted to conventional relational tables.
Major types:
  Document databases;
- Store records as documents, commonly JSON-like structures.
- Example: MongoDB.
- Suitable for flexible application data and nested records.
  Key-value databases;
- Store information as key-value pairs.
- Examples: Redis, Amazon DynamoDB.
- Suitable for caching, sessions, and fast lookups.
  Wide-column databases;
- Organize data using column families and distributed storage structures.
- Example: Apache Cassandra.
- Suitable for large-scale distributed workloads.
  Graph databases;
- Store entities as nodes and relationships as edges.
- Example: Neo4j.
- Suitable for social networks, recommendation systems, and relationship analysis.
  Time-series databases;
Optimized for timestamped measurements and events.
Examples:
- InfluxDB.
- TimescaleDB.
- Prometheus (primarily a time-series monitoring system).
Applications:
- IoT sensor monitoring.
- Industrial equipment monitoring.
- Network performance monitoring.
- Energy consumption tracking.
  In-memory databases;
Store data primarily in RAM to support very fast access.
Example: Redis.
Applications:
- Caching.
- Real-time analytics.
- Session management.
- Low-latency data access.
  Distributed databases;
Store and manage data across multiple interconnected machines.
Advantages:
- Horizontal scalability.
- High availability.
- Geographic distribution.
- Fault tolerance.
Challenges:
- Replication consistency.
- Network latency.
- Distributed transactions.
- Coordination and recovery.

 RELATIONAL DATABASE DESIGN
Relational database design organizes data into tables while minimizing unnecessary duplication and preserving relationships.
  Relationships between tables;
One-to-one (1:1)
One record in a table corresponds to one record in another table.
Example: a person and their unique identity profile.
One-to-many (1:M)
One record in a table can relate to multiple records in another table.
Example: one customer can place many orders.
Many-to-many (M:N)
Multiple records in one table can relate to multiple records in another.
Example: students can enroll in many courses, and each course can have many students.
Many-to-many relationships are usually implemented using a junction or associative table.
  Entity Relationship Diagrams (ERDs);
An ERD visually represents database entities, attributes, and relationships.
Main components:
- Entity: an object or concept, such as Student.
- Attribute: a property, such as Student_ID.
- Relationship: an association between entities.
- Cardinality: specifies how many instances can participate in a relationship.
ERDs are used during database planning and design.
  Normalization;
Normalization organizes relational data to reduce redundancy and prevent insertion, update, and deletion anomalies.
First Normal Form (1NF)
- Each column contains atomic values.
- No repeating groups or multivalued fields within a single cell.
- Each row can be uniquely identified.
Second Normal Form (2NF)
- Must satisfy 1NF.
- Every non-key attribute must depend on the whole candidate key, not just part of a composite candidate key.
Third Normal Form (3NF)
- Must satisfy 2NF.
- Non-key attributes must not have inappropriate transitive dependencies on candidate keys.
Boyce-Codd Normal Form (BCNF)
- Every determinant must be a candidate key (more precisely, a superkey).
Normalization improves data consistency and reduces duplication.
  Denormalization
Intentionally introduces controlled redundancy to improve query performance.
Applications:
- Analytical databases.
- Reporting systems.
- Read-heavy applications.
Trade-off: faster reads may come at the cost of more complex updates and additional storage.

 STRUCTURED QUERY LANGUAGE (SQL)
SQL is the standard language used to define, manipulate, query, and control data in relational database systems.
  SQL command categories;
DDL — Data Definition Language
Defines database structures.
Commands:
- CREATE
- ALTER
- DROP
- TRUNCATE
DML — Data Manipulation Language
Changes database records.
Commands:
- INSERT
- UPDATE
- DELETE
DQL — Data Query Language
Retrieves information.
Command:
- SELECT
DCL — Data Control Language
Controls access and permissions.
Commands:
- GRANT
- REVOKE
TCL — Transaction Control Language
Manages transactions.
Commands:
- COMMIT
- ROLLBACK
- SAVEPOINT
  Basic SQL operations;
CREATE TABLE:
Creates a new table.
INSERT:
Adds new records.
SELECT:
Retrieves records.
UPDATE:
Modifies existing records.
DELETE:
Removes selected records.
ALTER TABLE:
Changes a table structure.
DROP TABLE:
Removes a table and its definition.
TRUNCATE TABLE:
Removes all rows while retaining the table structure. Exact transactional and identity-reset behavior varies by DBMS.
  SQL filtering and sorting;
WHERE: filters records using conditions.
ORDER BY: sorts query results.
GROUP BY: groups records for aggregation.
HAVING: filters groups after aggregation.
DISTINCT: removes duplicate result rows.
LIMIT / FETCH / TOP: restricts the number of returned rows, depending on the DBMS.
  SQL operators;
- Arithmetic: +, -, *, /, %.
- Comparison: =, <>, !=, >, <, >=, <=.
- Logical: AND, OR, NOT.
- Pattern matching: LIKE.
- Range checking: BETWEEN.
- Membership: IN.
- Null checking: IS NULL, IS NOT NULL.
Important: NULL represents missing or unknown information; it should not be tested using = NULL.
  SQL aggregate functions;
- COUNT(): counts records or non-null values.
- SUM(): calculates a total.
- AVG(): calculates an average.
- MIN(): finds the minimum.
- MAX(): finds the maximum.
 
 SQL JOINS AND SUBQUERIES
  Joins;
Joins combine records from related tables.
INNER JOIN: returns matching records from both tables.
LEFT JOIN: returns all records from the left table and matching records from the right table; unmatched right-side columns are NULL.
RIGHT JOIN: returns all records from the right table and matching records from the left table.
FULL OUTER JOIN: returns matching and nonmatching records from both tables.
CROSS JOIN: returns the Cartesian product of two tables.
SELF JOIN: joins a table to itself.
  Subqueries;
A subquery is a query nested inside another SQL statement.
Applications:
- Filtering using another query's result.
- Comparing values against aggregated results.
- Checking whether related records exist.
- Producing derived values.
  Common Table Expressions (CTEs);
A CTE is a named temporary result set defined using WITH and available to the statement that follows it.
Useful for:
- Improving query readability.
- Breaking complex queries into logical steps.
- Recursive queries, such as hierarchical relationships.

 DATABASE TRANSACTIONS AND ACID PROPERTIES
A transaction is a logical unit of database operations that should be completed as a whole.
Example: transferring money between two bank accounts.
1. Deduct money from account A.
2. Add money to account B.
3. Commit both operations.
  ACID properties;
-Atomicity
All operations in a transaction succeed, or the transaction is rolled back.
-Consistency
A transaction preserves defined database integrity rules.
-Isolation
Concurrent transactions should behave according to the selected isolation level, preventing unacceptable interference.
-Durability
Once committed, changes survive failures according to the database's durability guarantees.
  Transaction commands;
- BEGIN / START TRANSACTION: starts a transaction.
- COMMIT: permanently commits changes.
- ROLLBACK: cancels uncommitted changes.
- SAVEPOINT: creates a point to which a transaction can partially roll back.
  Isolation levels;
- Read Uncommitted: may allow dirty reads where supported.
- Read Committed: prevents dirty reads.
- Repeatable Read: provides stronger protection against changes to previously read rows; exact phantom behavior varies by DBMS.
- Serializable: strongest standard isolation level; transactions behave as if executed sequentially.
  Common concurrency problems;
Dirty read: reading another transaction's uncommitted changes.
Non-repeatable read: retrieving a previously read row again and getting a different committed value.
Phantom read: repeating a query and finding new or missing rows that satisfy its search condition.
Lost update: one transaction overwrites another transaction's update.

 INDEXING AND QUERY OPTIMIZATION
  Database indexing;
An index is an auxiliary data structure that helps the DBMS locate records without scanning every row.
Common types:
B-tree index
- Supports equality and range searches.
- Common default index structure in relational databases.
Hash index
- Designed mainly for equality lookups.
- Does not generally support efficient range searches.
Composite index
- Uses multiple columns.
- Column order affects which query patterns can benefit.
Unique index
- Enforces uniqueness while supporting lookups.
Full-text index
- Supports efficient text-search operations.
  Index advantages;
- Faster data retrieval.
- Improved filtering.
- Efficient joins and sorting in suitable cases.
  Index disadvantages;
- Requires additional storage.
- Can slow INSERT, UPDATE, and DELETE operations.
- Requires maintenance.
  Query optimization;
Query optimization improves the efficiency of database queries.
Techniques:
- Index frequently filtered and joined columns where appropriate.
- Avoid SELECT * when only a few columns are required.
- Use efficient joins.
- Filter data early when beneficial.
- Avoid unnecessary nested queries.
- Analyze query execution plans.
- Avoid functions on indexed columns when they prevent efficient index use.
- Keep database statistics updated.
Use EXPLAIN or EXPLAIN ANALYZE, depending on the DBMS, to inspect query execution plans.

 DATABASE STORAGE AND INTERNAL ARCHITECTURE
A DBMS typically uses several internal structures to manage data.
  Storage components;
Data files: contain stored database records.
Pages/Blocks: fixed-size or managed units of database storage and I/O.
Indexes: accelerate data access.
Transaction logs: record changes used for recovery and durability.
Buffer pool/cache: holds frequently accessed database pages in memory.
  Write-Ahead Logging (WAL);
A recovery technique in which relevant log records are written to durable storage before the corresponding modified data pages are written.
Benefits:
- Crash recovery.
- Transaction durability.
- Replication support in some systems.
  Query processing;
A typical query execution process includes:
1. SQL parsing.
2. Syntax and semantic validation.
3. Query optimization.
4. Execution-plan generation.
5. Query execution.
6. Result delivery.
The optimizer chooses an execution strategy based on estimated costs, available indexes, statistics, and query structure.

 DATABASE REPLICATION AND SHARDING
  Replication;
Replication maintains copies of data across multiple database servers.
Types:
Primary-replica replication
- A primary database accepts writes.
- Replicas receive changes.
- Replicas can serve read workloads depending on configuration.
Multi-primary replication
- Multiple nodes can accept writes.
- Requires conflict management and consistency mechanisms.
Advantages:
- High availability.
- Read scalability.
- Disaster recovery support.
Challenges:
- Replication lag.
- Conflict resolution.
- Consistency management.
  Sharding;
Sharding divides a dataset into smaller partitions distributed across multiple database servers.
Example: customer records are distributed across database nodes using customer IDs.
Advantages:
- Horizontal scalability.
- Distributed storage.
- Potentially higher write capacity.
Challenges:
- Cross-shard queries.
- Rebalancing.
- Distributed transactions.
- Data skew.
  Replication vs sharding;
Replication creates multiple copies of data.
Sharding distributes different portions of data across nodes.
They can be combined in large distributed database systems.

 DISTRIBUTED DATABASES AND CAP THEOREM
The CAP theorem describes a trade-off in distributed systems during a network partition.
  The three properties are:
-Consistency (C): every read receives the latest successful write or an error, according to the formal model.
-Availability (A): every request to a non-failing node receives a response, although it may not contain the latest data.
-Partition Tolerance (P): the system continues operating despite communication failures between nodes.
When a network partition occurs, a distributed system cannot guarantee both perfect consistency and availability for every request.
It must make trade-offs in how it responds.
  Eventual consistency;
A consistency model in which replicas may temporarily contain different values but converge if updates stop and replication succeeds.
Common in some distributed NoSQL systems.

 DATABASE BACKUP AND RECOVERY
Backup and recovery protect databases against data loss, corruption, hardware failure, and accidental deletion.
  Backup types;
-Full backup: copies the entire database.
-Incremental backup: copies changes since the previous backup of any type.
-Differential backup: copies changes since the most recent full backup.
-Logical backup: exports database objects and records into a logical representation.
-Physical backup: copies database files or storage-level representations.
  Recovery techniques;
- Transaction log recovery.
- Point-in-time recovery.
- Replication and failover.
- Database restoration.
- Automated backup scheduling.
  Important concepts;
RPO (Recovery Point Objective): maximum acceptable data loss measured in time.
RTO (Recovery Time Objective): maximum acceptable time to restore service.
A backup is only useful if restoration has been tested.

 CLOUD DATABASES
Cloud databases are databases hosted on cloud infrastructure, either managed by a provider or operated by the organization on cloud-based virtual machines or containers.
  Cloud database service models;
Managed database services
The provider manages much of the infrastructure, backups, patching, and availability configuration.
Examples:
- Amazon RDS.
- Amazon Aurora.
- Azure SQL Database.
- Google Cloud SQL.
  Cloud-native data warehouses;
Optimized for analytical workloads.
Examples:
- Amazon Redshift.
- Google BigQuery.
- Snowflake.
  Cloud NoSQL services;
Examples:
- Amazon DynamoDB.
- Azure Cosmos DB.
- Google Firestore.
Benefits
- Elastic scalability.
- Managed maintenance.
- High availability options.
- Geographic deployment.
- Integration with cloud data pipelines.
Challenges
- Usage-based costs.
- Vendor dependency.
- Network latency.
- Data residency and privacy.
- Access management.
- Data transfer costs.

 DATABASES IN IoT SYSTEMS
IoT systems generate continuous streams of sensor readings, events, and device information.
Database selection depends on data volume, access patterns, latency, and retention requirements.
  Common IoT database requirements;
- High ingestion rates.
- Timestamp-based storage.
- Efficient historical queries.
- Device identification.
- Data retention policies.
- Time-series aggregation.
- Reliable handling of missing and duplicate readings.
  Example IoT data structure
A sensor reading may contain:
- Device_ID
- Timestamp
- Temperature
- Humidity
- Location
- Battery_Level
  Database selection;
Time-series database: sensor measurements and historical trends.
Relational database: device registration, user accounts, configuration, and transactional records.
NoSQL database: flexible device metadata and high-volume application records.
In-memory database: temporary device states, caching, and low-latency operations.
  Example architecture
ESP32 → MQTT Broker → Stream Processor → Time-Series Database → Analytics Dashboard.

 DATABASE SECURITY
Database security protects stored information and prevents unauthorized access or modification.
  Essential security practices;
- Authentication: verifies user or application identity.
- Authorization: determines permitted operations.
- Role-Based Access Control (RBAC): assigns permissions through roles.
- Encryption at rest: protects stored data.
- Encryption in transit: protects network communication.
- Auditing: records important database activities.
- Backup protection: secures backup files and recovery credentials.
- Parameterized queries: prevent SQL injection.
- Least privilege: grants only necessary permissions.
- Data masking: conceals sensitive information where appropriate.
  SQL injection;
A vulnerability in which malicious input changes the intended meaning of an SQL statement.
Prevention:
- Use parameterized queries or prepared statements.
- Avoid constructing SQL by concatenating untrusted input.
- Validate input.
- Restrict database privileges.
- Avoid exposing database error details unnecessarily.

 DATABASE PERFORMANCE METRICS
  Important measurements include:
- Query response time.
- Transaction throughput.
- Transactions per second (TPS).
- Queries per second (QPS).
- Cache hit ratio.
- Index efficiency.
- CPU and memory utilization.
- Disk I/O performance.
- Connection count.
- Lock contention.
- Replication lag.
- Database availability.
   Important equations;
1. Query response time
Response time = Completion time − Request time
2. Transaction throughput
TPS = Number of completed transactions / Time in seconds
3. Cache hit ratio
Cache hit ratio (%) = Cache hits / (Cache hits + Cache misses) × 100
4. Database availability
Availability (%) = Uptime / (Uptime + Downtime) × 100
5. Storage utilization
Storage utilization (%) = Used storage / Total available storage × 100
6. Data transfer time
Transfer time = Data size / Effective transfer rate
Ensure data size and transfer rate use compatible units.

 PRACTICAL DATABASE DEVELOPMENT WORKFLOW
A typical database development process:
1. Identify system requirements.
2. Identify entities and their attributes.
3. Define relationships between entities.
4. Draw an Entity Relationship Diagram.
5. Select an appropriate database model.
6. Normalize the relational schema where appropriate.
7. Define tables, data types, keys, and constraints.
8. Implement the database.
9. Populate it with test data.
10. Develop queries and application interfaces.
11. Implement security and access control.
12. Test correctness and performance.
13. Configure backup and recovery.
14. Deploy and monitor the database.
15. Maintain and optimize as requirements evolve.
  Database testing;
- Functional testing.
- Constraint and integrity testing.
- Transaction testing.
- Security testing.
- Performance and load testing.
- Backup and recovery testing.
- Replication and failover testing.

 IMPORTANT DATABASE TECHNOLOGIES
Technology| Main application
PostgreSQL| Advanced relational database
MySQL| Relational web and application databases
SQLite| Lightweight embedded relational database
Microsoft SQL Server| Enterprise relational database
Oracle Database| Enterprise database management
MongoDB| Document-oriented NoSQL database
Redis| In-memory key-value database
Apache Cassandra| Distributed wide-column database
Neo4j| Graph database
InfluxDB| Time-series database
TimescaleDB| PostgreSQL-based time-series extension
Amazon DynamoDB| Managed cloud key-value/document database

 IMPORTANT ENGINEERING TIPS
1. Choose a database based on data structure, query patterns, consistency, and scale rather than popularity.
2. Define primary and foreign keys correctly.
3. Use appropriate data types to avoid unnecessary storage and conversion overhead.
4. Apply normalization to reduce redundancy in transactional databases.
5. Use denormalization selectively for performance.
6. Index frequently queried columns based on actual query patterns.
7. Avoid excessive indexing because indexes increase write and storage costs.
8. Use transactions for operations that must succeed or fail together.
9. Always use parameterized queries when handling external input.
10. Automate backups and test restoration.
11. Monitor query performance and database resource utilization.
12. Plan for growth, replication, and recovery.
13. Separate application permissions from database administration privileges.
14. Document database schemas and relationships.
15. Never assume that replication alone is a complete backup strategy.

 SUMMARY
Databases provide the foundation for storing, organizing, retrieving, and managing information in modern computing systems.
  Key concepts:
- DBMS: software for managing databases.
- SQL: language for relational database operations.
- NoSQL: alternative database models for different data requirements.
- Keys and constraints: establish identity and integrity.
- Normalization: reduces redundancy and anomalies.
- Relationships: connect related entities.
- Transactions and ACID: maintain reliable operations.
- Indexing: improves data retrieval.
- Replication: maintains copies of data.
- Sharding: distributes data across multiple nodes.
- Cloud databases: provide managed and scalable database infrastructure.
- IoT databases: handle continuous sensor readings and time-series information.
- Security and recovery: protect data and maintain availability.

The central engineering principle is to select, design, and manage a database that stores the right data, maintains its integrity, supports required access patterns, and delivers reliable performance as the system grows.