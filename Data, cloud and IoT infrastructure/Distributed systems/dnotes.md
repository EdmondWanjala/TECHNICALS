                DISTRIBUTED SYSTEMS 
A distributed system is a collection of independent computers (nodes) connected through a network that communicate and coordinate their operations to achieve a common objective.
Although each computer operates independently, the system is designed to function as a coordinated whole.
  Examples:
- Cloud computing platforms.
- Distributed databases.
- Banking transaction systems.
- Global content delivery networks (CDNs).
- IoT sensor networks.
- Distributed data-processing platforms.
- Microservices-based applications.
  Main objectives;
- Scalability: increase system capacity as demand grows.
- Reliability: maintain correct operation despite component failures.
- Availability: keep services accessible.
- Fault tolerance: continue operating despite failures.
- Performance: distribute workloads to improve processing efficiency.
- Resource sharing: share storage, computing power, and services.
- Geographic distribution: serve users and devices from multiple locations.
  Basic architecture;
Node A + Node B + Node C + ... + Node N → Network Communication → Coordinated System
Each node can perform computations, store information, and communicate with other nodes.

 FUNDAMENTAL CONCEPTS
  Nodes;
A node is an individual computing device or process participating in a distributed system.
Examples:
- Physical servers.
- Virtual machines.
- Cloud instances.
- Containers.
- IoT gateways.
- Edge devices.
  Communication;
Nodes exchange information through network protocols and messaging systems.
Common communication methods:
- TCP/IP sockets.
- HTTP/HTTPS.
- REST APIs.
- gRPC.
- Message queues.
- Publish-subscribe messaging.
  Distributed processing;
A large task is divided into smaller tasks that can be executed across multiple nodes.
Example: processing a dataset of 1 TB by dividing it into smaller partitions and distributing the processing workload across several servers.
  Resource sharing;
Nodes share:
- Processing power.
- Storage.
- Databases.
- Network resources.
- Applications and services.
  Concurrency;
Multiple processes or operations execute at overlapping times across different nodes.
Concurrency introduces challenges such as:
- Race conditions.
- Data conflicts.
- Deadlocks.
- Synchronization problems.
- Inconsistent updates.

 DISTRIBUTED SYSTEM ARCHITECTURES
  Client-server architecture;
Clients request services from centralized or distributed servers.
Example:
A mobile application sends a request to a server, which retrieves information from a database and returns a response.
Advantages:
- Centralized service management.
- Easier access control.
- Clear separation of clients and services.
Limitations:
- Server bottlenecks.
- Potential single points of failure if redundancy is absent.
  Peer-to-peer (P2P) architecture;
Nodes communicate and share resources directly without relying entirely on a central server.
Examples:
- BitTorrent.
- Certain blockchain networks.
- Decentralized communication systems.
Advantages:
- Resource sharing.
- Reduced dependence on central infrastructure.
- Potential horizontal scalability.
Challenges:
- Peer discovery.
- Security.
- Coordination.
- Unreliable or frequently changing nodes.
  Master-worker architecture;
A master or coordinator assigns tasks to worker nodes.
Example:
A distributed processing system divides a large dataset into partitions and assigns them to multiple workers.
The coordinator may distribute tasks, monitor execution, and collect results.
  Microservices architecture;
An application is divided into small, independently deployable services communicating over a network.
Example:
An e-commerce application may have:
- User service.
- Product service.
- Payment service.
- Inventory service.
- Notification service.
Advantages:
- Independent deployment.
- Technology flexibility.
- Independent scaling.
- Better separation of responsibilities.
Challenges:
- Network communication complexity.
- Distributed transactions.
- Service discovery.
- Monitoring and debugging.
- Security across service boundaries.
  Layered architecture;
Organizes distributed applications into logical layers, such as:
- Presentation layer.
- Application or service layer.
- Data layer.
Each layer provides services to the layer above it.

 COMMUNICATION IN DISTRIBUTED SYSTEMS
Communication enables nodes to exchange commands, data, and coordination information.
  Message passing;
Nodes exchange messages rather than sharing a common memory space.
Types:
Synchronous communication
- Sender and receiver coordinate during an interaction.
- A sender may wait for a response.
- Example: synchronous HTTP request-response.
Asynchronous communication
- Sender transmits a message without waiting for the receiver to complete processing.
- Messages may be buffered in a queue or broker.
- Example: Kafka or RabbitMQ messaging.
  Remote Procedure Call (RPC);
RPC allows a program to invoke a procedure on another computer as though it were a local function call.
The underlying system handles network communication and remote execution.
Examples:
- gRPC.
- XML-RPC.
- JSON-RPC.
Important: remote calls can fail because of network interruptions, timeouts, or server failures, unlike ordinary local function calls.
  REST APIs;
REST is an architectural style commonly used for communication between distributed services.
Common HTTP methods:
- GET: retrieve resources.
- POST: create or submit resources.
- PUT: replace a resource.
- PATCH: partially update a resource.
- DELETE: remove a resource.
  Publish-subscribe architecture;
Producers publish messages to topics or channels, and consumers subscribe to receive relevant messages.
Example:
An IoT sensor publishes temperature readings to an MQTT topic, and multiple monitoring applications subscribe to it.
Advantages:
- Loose coupling.
- Multiple consumers.
- Asynchronous communication.
- Easy integration of new services.

 DISTRIBUTED SYSTEM SCALABILITY
Scalability is the ability of a system to handle increased workloads by expanding its available resources.
  Vertical scaling (Scale-up);
Increasing the resources of an existing machine.
Examples:
- More RAM.
- Faster CPU.
- Larger storage.
- Higher network capacity.
Advantages:
- Simpler architecture.
- Often requires fewer distributed coordination mechanisms.
Limitations:
- Hardware limits.
- Potentially high upgrade costs.
- May retain a single point of failure.
  Horizontal scaling (Scale-out);
Adding more machines or nodes to distribute the workload.
Advantages:
- Greater potential capacity.
- Supports distributed fault tolerance.
- Suitable for large-scale applications.
Limitations:
- Requires coordination.
- Introduces network overhead.
- Requires workload distribution and data management.
  Load balancing;
Distributes incoming requests across multiple servers to prevent overloading individual nodes.
Common algorithms:
Round Robin: distributes requests sequentially.
Weighted Round Robin: distributes requests according to assigned server weights.
Least Connections: sends requests to the server with the fewest active connections.
IP Hash: uses client IP information to select a server.
  Auto-scaling;
Automatically increases or decreases computing resources based on workload demand or predefined policies.
Example:
A cloud platform adds application instances when request volume increases and removes excess instances when demand falls.

 DISTRIBUTED DATA STORAGE
Distributed storage allows data to be stored across multiple computers while providing coordinated access.
  Data partitioning;
Divides a dataset into smaller sections distributed across nodes.
Horizontal partitioning (sharding): distributes different rows or records across nodes.
Vertical partitioning: separates columns or groups of attributes into different storage structures.
Hash partitioning: distributes records using a hash function.
Range partitioning: distributes records based on value ranges.
Example:
Customer records with IDs 1–100,000 are stored on one shard, while other ranges are assigned to different shards.
  Data replication;
Maintains multiple copies of data across different nodes.
Types:
Synchronous replication
- Updates are coordinated with replicas before the write is acknowledged according to the configured consistency guarantees.
- Can improve consistency but may increase write latency.
Asynchronous replication
- Changes are propagated to replicas after the primary system acknowledges the write.
- Can reduce latency but introduces replication lag and potential data loss during failures.
  Distributed file systems;
Store files across multiple machines while presenting a unified storage environment.
Examples:
- Hadoop Distributed File System (HDFS).
- Google File System (GFS).
- Ceph.
- GlusterFS.
Applications:
- Big-data processing.
- Large-scale file storage.
- Distributed analytics.
- Cloud infrastructure.

 DISTRIBUTED SYSTEM CONSISTENCY
Consistency describes how data changes are observed across nodes and replicas.
  Strong consistency;
After a successful write, subsequent reads are guaranteed to observe that write, according to the system's consistency model.
Useful for:
- Financial transactions.
- Critical inventory operations.
- Systems requiring strongly coordinated state.
  Eventual consistency;
Replicas may temporarily contain different values but are expected to converge if updates stop and communication succeeds.
Useful for:
- Distributed caching.
- Social media feeds.
- Globally distributed applications.
- Systems prioritizing availability and low latency.
  Read-your-writes consistency;
A client can observe its own successful writes in subsequent reads.
  Causal consistency;
Operations that are causally related are observed in an order that respects their causal dependencies.
  Quorum-based consistency;
Uses a required number of nodes to acknowledge reads or writes.
For a replicated dataset with N replicas:
- W = number of replicas required to acknowledge a write.
- R = number of replicas consulted for a read.
- N = total number of replicas.
A common condition for overlapping read and write replica sets is:
    R + W > N
For example:
N = 3, W = 2, R = 2.
This overlap can help reads observe recent writes, but actual guarantees depend on replica selection, failure handling, and the database's consistency protocol.

 THE CAP THEOREM
The CAP theorem describes the fundamental trade-off in distributed systems when a network partition occurs.
  The three properties are:
Consistency (C):
Every read receives the latest successful write or an error, according to the formal CAP definition.
Availability (A):
Every request to a non-failing node receives a response, even if it may not contain the latest data.
Partition Tolerance (P):
The system continues operating despite network communication failures between nodes.
CAP principle
When a network partition occurs, a distributed system cannot simultaneously guarantee both perfect consistency and availability for every request.
It must make a trade-off between consistency and availability during the partition.
- CP-oriented behavior: preserves consistency, potentially rejecting or delaying some requests.
- AP-oriented behavior: continues responding, potentially returning stale or conflicting information.
Partition tolerance is essential in real distributed environments because network failures cannot be completely eliminated.

 FAULT TOLERANCE AND HIGH AVAILABILITY
  Fault tolerance;
The ability of a distributed system to continue operating correctly despite failures of individual components.
Possible failures:
- Server crashes.
- Network interruptions.
- Power failures.
- Storage failures.
- Software errors.
- Hardware faults.
  Redundancy;
Providing additional resources or components so that the failure of one does not necessarily stop the system.
Examples:
- Multiple servers.
- Replicated databases.
- Redundant network connections.
- Backup power supplies.
  Failover;
Automatically or manually transferring operations from a failed component to a functioning alternative.
  Fault detection;
Identifies unavailable or malfunctioning nodes.
Methods:
- Heartbeat messages.
- Health checks.
- Timeouts.
- Monitoring metrics.
- Failure detectors.
  Checkpointing;
Periodically saves the current processing state so computation can resume after failure.
  Disaster recovery;
Procedures and infrastructure used to restore services after major failures.
Important metrics:
- RTO: maximum acceptable recovery time.
- RPO: maximum acceptable data loss measured in time.

 DISTRIBUTED COORDINATION AND CONSENSUS
Distributed nodes often need to agree on shared decisions, such as which node is the leader or which update is accepted.
  Leader election;
The process of selecting one node to coordinate specific system operations.
The leader may:
- Coordinate writes.
- Manage task assignments.
- Maintain ordering.
- Coordinate membership changes.
  Consensus
The process by which distributed nodes agree on a value or sequence of operations despite certain failures.
Important consensus algorithms:
Raft
- A consensus algorithm designed to be understandable.
- Uses leader election and replicated logs.
- Supports agreement on an ordered sequence of commands.
Paxos
- A family of consensus algorithms.
- Enables distributed nodes to agree on values despite certain failures.
Practical Byzantine Fault Tolerance (PBFT)
- A consensus approach designed to tolerate certain malicious or arbitrary node behavior under specified assumptions.
  Distributed locking;
Coordinates access to shared resources so conflicting operations do not occur simultaneously.
Examples:
- Preventing two workers from processing the same job.
- Coordinating updates to shared records.
Distributed locks require careful handling of timeouts, leases, and node failures.

 DISTRIBUTED TRANSACTIONS
A distributed transaction involves operations across multiple databases, services, or nodes that need coordinated outcomes.
  Two-Phase Commit (2PC);
A protocol for coordinating a transaction across multiple participants.
Phase 1: Prepare
- Coordinator asks participants whether they can commit.
- Each participant prepares and votes YES or NO.
Phase 2: Commit or Abort
- If all participants vote YES, the coordinator instructs them to commit.
- If any participant votes NO, the coordinator instructs them to abort.
Advantages:
- Supports atomic commitment across participants under its protocol assumptions.
Limitations:
- Can block if the coordinator fails at critical stages.
- Adds coordination overhead.
- May reduce availability during failures.
  Saga pattern;
Manages a long-running distributed transaction as a sequence of local transactions.
If a step fails, compensating transactions attempt to reverse the effects of completed steps.
Example: an online purchase.
1. Reserve product.
2. Process payment.
3. Arrange delivery.
If payment fails, the product reservation can be cancelled.
Sagas are useful in microservices architectures where a single global database transaction is impractical.

 DISTRIBUTED COMPUTING AND PARALLEL PROCESSING
Distributed computing uses multiple networked computers to solve computational problems.
  Parallel processing;
Divides a computation into independent or partially independent tasks that execute simultaneously.
  MapReduce;
A programming model for processing large datasets across distributed nodes.
Map phase
- Processes input records.
- Produces intermediate key-value pairs.
Shuffle and sort
- Groups intermediate values by key.
Reduce phase
- Aggregates values associated with each key.
Example: counting words in a large collection of documents.
  Apache Hadoop;
An ecosystem for distributed data storage and processing.
Important components:
- HDFS: distributed file storage.
- MapReduce: distributed processing model.
- YARN: cluster resource management.
  Apache Spark;
A distributed processing engine used for:
- Batch processing.
- SQL analytics.
- Machine learning workloads.
- Stream processing.
Spark can execute computations across a cluster and uses optimized execution plans.

  Parallelism vs concurrency;
Concurrency: multiple tasks make progress during overlapping periods.
Parallelism: multiple tasks execute simultaneously on different processing resources.
Parallelism is one way of achieving concurrency, but the terms are not interchangeable.

 MICROSERVICES AND SERVICE DISCOVERY
  Microservices;
An architectural approach in which an application is divided into small services, each responsible for a specific business capability.
Characteristics:
- Independently deployable services.
- Network-based communication.
- Separate service responsibilities.
- Independent scaling.
- Often independent data ownership.
  API Gateway;
A central entry point through which clients access multiple backend services.
Functions:
- Request routing.
- Authentication.
- Rate limiting.
- Request transformation.
- Logging.
  Service discovery;
Allows services to find the network locations of other services dynamically.
Types:
- Client-side discovery.
- Server-side discovery.
Technologies include Consul, Kubernetes service discovery, and DNS-based mechanisms.
  Container orchestration;
Manages the deployment and operation of containerized applications across a cluster.
Kubernetes supports:
- Container scheduling.
- Service discovery.
- Scaling.
- Health checks.
- Rolling deployments.
- Workload recovery.

 DISTRIBUTED SYSTEMS IN CLOUD COMPUTING
Cloud infrastructure heavily relies on distributed systems.
  Common cloud components;
- Distributed storage.
- Virtual machines and containers.
- Load balancers.
- Distributed databases.
- Messaging services.
- Content delivery networks.
- Distributed monitoring systems.
  Cloud deployment concepts;
Availability zones: separate infrastructure locations within a cloud region designed to reduce correlated failures.
Regions: geographic cloud deployment areas.
Auto-scaling: automatically adjusts resources according to demand.
Content Delivery Networks (CDNs): distribute cached content across geographically distributed edge locations to reduce delivery latency.
Examples of cloud technologies
- AWS: EC2, S3, DynamoDB, EKS.
- Microsoft Azure: Virtual Machines, Blob Storage, Cosmos DB, AKS.
- Google Cloud: Compute Engine, Cloud Storage, Spanner, GKE.

 DISTRIBUTED SYSTEMS IN IoT AND EDGE COMPUTING
IoT systems often consist of thousands or millions of geographically distributed devices communicating with cloud and edge infrastructure.
  Typical architecture;
Sensors → Microcontrollers → Edge Gateways → Network → Cloud Platform → Distributed Storage and Analytic
  Applications;
Smart agriculture
- Distributed soil and weather sensors.
- Centralized or distributed monitoring.
- Automated irrigation control.
Industrial automation
- Machines communicate with edge gateways.
- Local processing detects abnormal conditions.
- Cloud systems analyze historical performance.
Smart cities
- Distributed traffic sensors.
- Smart lighting.
- Environmental monitoring.
- Public infrastructure management.
Edge computing
Processes data near its source instead of transmitting all raw data to a centralized cloud.
Advantages:
- Lower response latency.
- Reduced bandwidth consumption.
- Local operation during network failures.
- Improved data privacy in suitable designs.
Fog computing
Extends cloud capabilities into intermediate network layers between edge devices and centralized cloud infrastructure.
It provides distributed processing, storage, and communication closer to IoT devices.

 DISTRIBUTED SYSTEM SECURITY
Distributed systems introduce security challenges because data and services communicate across multiple network locations.
  Essential security mechanisms;
Authentication: verifies the identity of users, devices, and services.
Authorization: determines which operations an authenticated entity can perform.
Encryption: protects data in transit and at rest.
Mutual TLS (mTLS): enables both communicating services to authenticate each other using certificates.
Access control: restricts access to resources.
Network segmentation: separates infrastructure into controlled network zones.
Secrets management: securely stores credentials, API keys, and certificates.
Auditing: records security-relevant activities.
Zero Trust: security approach based on continuously verifying access rather than automatically trusting entities because of their network location.
  Common threats;
- Denial-of-service attacks.
- Man-in-the-middle attacks.
- Credential theft.
- Unauthorized service access.
- Data interception.
- Compromised nodes.
- Software supply-chain attacks.

 DISTRIBUTED SYSTEM PERFORMANCE AND EQUATIONS
  Speedup;
Measures how much faster a task executes using parallel processing.
    Speedup = T₁ / Tₙ
Where:
- T₁ = execution time on one processor.
- Tₙ = execution time using n processors.
Example:
T₁ = 100 seconds
T₄ = 30 seconds
Speedup = 100 / 30 = 3.33
The four-processor system is approximately 3.33 times faster.
  Efficiency;
Measures how effectively processing resources are utilized.
Efficiency = Speedup / Number of processors
Efficiency (%) = (Speedup / n) × 100
Using the previous example:
Efficiency = (3.33 / 4) × 100 = 83.25%
  Amdahl's Law;
Estimates the maximum speedup achievable through parallel processing when part of a task must remain sequential.
    S(n) = 1 / [(1 − P) + P/n]
Where:
- P = parallelizable fraction.
- n = number of processors.
- 1 − P = sequential fraction.
If 90% of a task is parallelizable and 4 processors are used:
S(4) = 1 / [0.1 + (0.9/4)]
S(4) = 1 / 0.325
    S(4) ≈ 3.08
This demonstrates that the sequential portion limits the total speedup.
  Network latency;
Network latency = Receiving time − Sending time
For round-trip time (RTT), measure the time between sending a request and receiving its response.
  Throughput;
Throughput = Total work completed / Time taken
Examples:
- Requests per second.
- Transactions per second.
- Messages per second.
- Bytes per second.
  Availability;
Availability = Uptime / (Uptime + Downtime)
Availability (%) = [Uptime / (Uptime + Downtime)] × 100
  Reliability of series components;
For independent components where all must work:
    R(system) = R₁ × R₂ × ... × Rₙ
For n identical independent components:
    R(system) = Rⁿ
  Reliability of parallel redundant components;
For independent redundant components where at least one must work:
    R(system) = 1 − [(1 − R₁)(1 − R₂)...(1 − Rₙ)]
For two identical independent components:
    R(system) = 1 − (1 − R)²
These simplified reliability formulas assume independent failures.
  Little's Law;
L = λW
Where:
- L = average number of items in a system.
- λ = average arrival or throughput rate.
- W = average time an item spends in the system.
Useful for analyzing queues, message brokers, and distributed processing systems.

 CHALLENGES IN DISTRIBUTED SYSTEMS
1. Network failures: communication between nodes may be interrupted.
2. Latency: remote operations take longer than local operations.
3. Partial failures: some components fail while others remain operational.
4. Data consistency: replicas may temporarily contain different values.
5. Synchronization: coordinating concurrent operations is difficult.
6. Security: multiple nodes and communication channels increase the attack surface.
7. Scalability: additional nodes introduce coordination and data-distribution overhead.
8. Debugging: failures may involve multiple services and machines.
9. Clock synchronization: different nodes may have different local clock readings.
10. Resource management: CPU, memory, storage, and network resources must be coordinated.
  Clock synchronization;
Distributed computers cannot assume their physical clocks are perfectly synchronized.
  Important concepts:
- NTP: Network Time Protocol, used to synchronize clocks.
- Logical clocks: track causal ordering without requiring perfectly synchronized physical clocks.
- Lamport timestamps: provide a way to order events consistently with causality.
- Vector clocks: help identify causal relationships and concurrent events.
A timestamp alone does not always establish the true order of distributed events.

 PRACTICAL DEVELOPMENT WORKFLOW
A typical distributed-system development process:
1. Define system requirements and performance objectives.
2. Identify services, nodes, and their responsibilities.
3. Choose the architecture.
4. Define communication protocols and data formats.
5. Design data partitioning and replication.
6. Implement service communication.
7. Configure load balancing and service discovery.
8. Implement fault detection and recovery.
9. Establish consistency and transaction requirements.
10. Implement authentication and authorization.
11. Deploy services using containers or cloud infrastructure.
12. Configure monitoring, logging, and tracing.
13. Conduct load, failure, and security testing.
14. Optimize performance and operational costs.
  Testing methods;
- Unit testing.
- Integration testing.
- Distributed transaction testing.
- Load testing.
- Stress testing.
- Network failure testing.
- Chaos engineering.
- Recovery and failover testing.
- Security testing.

 IMPORTANT DISTRIBUTED SYSTEM TECHNOLOGIES
Technology| Main application
Apache Kafka| Distributed event streaming
Apache Spark| Distributed data processing
Apache Hadoop| Distributed storage and processing
Kubernetes| Container orchestration
Docker| Application containerization
gRPC| Remote procedure communication
RabbitMQ| Message brokering
Apache Cassandra| Distributed NoSQL database
MongoDB| Document database with distributed deployment options
Redis| In-memory data storage and distributed caching
Consul| Service discovery and coordination
etcd| Distributed key-value storage and coordination
Prometheus| Metrics monitoring
Grafana| Monitoring and visualization
Nginx| Reverse proxy and load balancing

 IMPORTANT ENGINEERING TIPS
1. Design for network failures; never assume communication is always reliable.
2. Use timeouts for remote service calls.
3. Implement retries carefully, preferably with exponential backoff and jitter.
4. Make operations idempotent where possible.
5. Use load balancing to distribute requests.
6. Choose consistency requirements according to application needs.
7. Avoid unnecessary distributed transactions.
8. Use message queues to decouple independent services.
9. Monitor latency, throughput, availability, and error rates.
10. Plan for node failure, replication lag, and recovery.
11. Secure communication between services.
12. Use containers and orchestration when they provide real operational benefits.
13. Avoid creating too many microservices for a small application.
14. Test failure scenarios rather than testing only normal operation.
15. Keep architecture as simple as possible while meeting scalability and reliability requirements.

 SUMMARY
Distributed systems allow multiple independent computers to work together as a coordinated system.
  The main concepts are:
- Nodes: individual participating computers or processes.
- Communication: exchange of messages and information.
- Distributed processing: sharing computational workloads.
- Scalability: expanding system capacity.
- Load balancing: distributing incoming requests.
- Partitioning: dividing data across nodes.
- Replication: maintaining copies of data.
- Consistency: controlling how updates are observed.
- CAP theorem: consistency and availability trade-offs during network partitions.
- Fault tolerance: continued operation despite failures.
- Consensus: agreement between distributed nodes.
- Microservices: independently deployable application services.
- Distributed transactions: coordinating operations across systems.
- Cloud and edge computing: distributing computing resources geographically.
- Security: protecting distributed resources and communication.

The central engineering principle is to build systems that can coordinate multiple independent computing resources reliably, securely, and efficiently despite network delays, failures, and changing workloads.