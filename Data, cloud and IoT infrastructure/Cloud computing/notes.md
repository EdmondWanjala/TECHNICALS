            CLOUD COMPUTING INFRASTRUCTURE
Cloud computing is the delivery of computing resources and services over the internet, allowing users to access processing power, storage, databases, networking, software and other IT resources on demand without owning and maintaining all the underlying physical infrastructure.
Cloud computing infrastructure refers to the hardware and software resources that provide these services, including servers, storage systems, networks, virtualisation technologies, data centres and cloud management platforms.
  Main characteristics;
- On-demand self-service: Users can provision computing resources when required.
- Broad network access: Services are accessible through networks and different devices.
- Resource pooling: Computing resources are shared among multiple users.
- Rapid elasticity: Resources can scale up or down according to demand.
- Measured service: Resource usage is monitored and billed according to consumption.
  Applications;
- Website and application hosting.
- Data storage and backup.
- Artificial intelligence and machine learning.
- Big data processing and analytics.
- IoT infrastructure.
- Software development and testing.
- Enterprise systems.
- Disaster recovery.

 Cloud Computing Architecture
Cloud architecture consists of interconnected components that provide computing services.
  Front-End;
The client side through which users access cloud services.
Components:
- Web browsers.
- Mobile applications.
- Desktop applications.
- Client interfaces and APIs.
  Back-End;
The cloud provider's infrastructure responsible for processing and managing services.
Components:
- Physical servers.
- Virtual machines.
- Storage systems.
- Databases.
- Networking infrastructure.
- Virtualisation software.
- Security and management systems.
  Network;
Connects users to cloud infrastructure and enables communication between cloud services.
Examples:
- Internet.
- Private networks.
- Virtual Private Clouds (VPCs).
- VPN connections.
- Dedicated network connections.
  Cloud Management Layer;
Coordinates and controls cloud resources.
Functions include:
- Resource provisioning.
- Monitoring.
- Load balancing.
- Scaling.
- Billing.
- Security management.
- Fault detection and recovery.
  Basic architecture;
User / Client → Internet / Network → Cloud Infrastructure → Computing, Storage, Databases and Applications.

 Cloud Computing Service Models
Cloud services are classified according to how much of the computing infrastructure is managed by the provider and how much is controlled by the customer.
  Infrastructure as a Service (IaaS);
Provides virtualised computing infrastructure over the internet.
Resources provided:
- Virtual machines.
- Virtual storage.
- Virtual networks.
- Firewalls.
- Load balancers.
The customer manages the operating system, applications, data and much of the configuration.
Examples:
- Amazon EC2.
- Azure Virtual Machines.
- Google Compute Engine.
Applications: Server hosting, custom computing environments, development and testing.
  Platform as a Service (PaaS);
Provides a managed environment for developing, deploying and running applications without requiring users to manage the underlying servers and operating systems.
Resources provided:
- Application runtime environments.
- Development tools.
- Managed databases.
- Application hosting.
- Deployment and scaling services.
Examples:
- Google App Engine.
- Azure App Service.
- Heroku.
Applications: Web applications, APIs and software development.
  Software as a Service (SaaS);
Provides ready-to-use software applications over the internet.
Users access the software without managing the underlying infrastructure or application platform.
Examples:
- Google Workspace.
- Microsoft 365.
- Salesforce.
- Dropbox.
Applications: Email, collaboration, document management and customer relationship management.
  Comparison;
Feature| IaaS| PaaS| SaaS
Main provision| Infrastructure| Application platform| Complete software
User manages| OS, applications, data| Applications and data| Mainly usage and data settings
Provider manages| Physical infrastructure and virtualisation| Infrastructure and platform| Entire application stack
Flexibility| High| Moderate| Limited
Typical user| System administrators| Developers| End users
  Memory tip:;
- IaaS = Rent computing infrastructure.
- PaaS = Rent an application development platform.
- SaaS = Use ready-made software.

 Cloud Deployment Models
Deployment models describe where cloud infrastructure is hosted and who can access or control it.
  Public Cloud;
Infrastructure is owned and operated by a cloud provider and shared among multiple customers through logically isolated environments.
Examples: AWS, Microsoft Azure and Google Cloud.
Advantages:
- Low initial infrastructure cost.
- High scalability.
- Global availability.
- Reduced hardware maintenance.
Disadvantages:
- Dependence on provider infrastructure.
- Possible data residency and compliance challenges.
- Costs can increase with usage.
  Private Cloud;
Cloud infrastructure is dedicated to a single organisation.
It may be hosted within the organisation's premises or by an external provider.
Advantages:
- Greater control.
- Customised security and configurations.
- Suitable for specialised regulatory requirements.
Disadvantages:
- Higher setup and maintenance costs.
- Requires technical expertise.
- Scaling may require additional investment.
  Hybrid Cloud;
Combines private and public cloud environments, allowing data and applications to operate across both.
Example: A bank stores sensitive information in a private environment while using public cloud resources for less sensitive applications.
Advantages:
- Flexible workload placement.
- Greater control over sensitive data.
- Access to public cloud scalability.
  Community Cloud;
Infrastructure is shared by organisations with similar requirements, such as security, regulatory or operational needs.
Example: Several government institutions sharing a cloud environment.

 Data Centres and Cloud Infrastructure
A data centre is a physical facility containing computing and networking equipment used to store, process and distribute data.
  Main components;
1. Servers: Provide processing and memory resources.
2. Storage systems: Store operating systems, applications, databases and user data.
3. Networking equipment: Switches, routers, firewalls and network interfaces connect systems.
4. Power systems: Uninterruptible Power Supplies (UPS), backup generators and power distribution systems maintain electrical availability.
5. Cooling systems: Remove heat generated by servers and networking equipment.
6. Physical security: Access control, surveillance and environmental monitoring protect infrastructure.
  Data centre design considerations;
- Redundancy.
- Power efficiency.
- Cooling efficiency.
- Network capacity.
- Physical security.
- Fire protection.
- Availability and disaster recovery.
  Power Usage Effectiveness (PUE);
PUE measures data centre energy efficiency.
    PUE={Total Facility Energy}/{IT Equipment Energy}
A PUE value closer to 1 indicates that less additional energy is being used for cooling, power distribution and other facility operations.

 Virtualisation;
Virtualisation is the technology of creating virtual versions of computing resources, such as servers, operating systems, storage and networks.
It allows multiple isolated computing environments to operate on the same physical hardware.
  Hypervisor;
A hypervisor is software that creates and manages virtual machines (VMs).
Type 1: Bare-metal hypervisor
Runs directly on physical hardware.
Examples:
- VMware ESXi.
- Microsoft Hyper-V.
- Xen.
Type 2: Hosted hypervisor
Runs as an application on an existing operating system.
Examples:
- Oracle VirtualBox.
- VMware Workstation.
  Virtual Machine (VM);
A VM is a software-based computer with virtual CPU, memory, storage and networking resources.
Each VM can run its own operating system.
Advantages of virtualisation
- Better hardware utilisation.
- Reduced infrastructure costs.
- Isolation between workloads.
- Easier resource allocation.
- Faster deployment.
- Simplified backup and migration.
Limitations
- Resource contention.
- Virtualisation overhead.
- Management complexity.
- Potential impact when a physical host fails.

 Containers and Containerisation
Containerisation packages an application and its dependencies into an isolated, portable environment called a container.
Unlike a typical VM, a container shares the host operating system kernel.
  Containers vs Virtual Machines;
Feature| Virtual Machine| Container
Operating system| Each VM has its own guest OS| Shares host kernel
Size| Generally larger| Generally smaller
Startup| Usually slower| Usually faster
Isolation| Virtual hardware and OS boundary| OS-level isolation
Resource usage| Generally higher| Generally lower
Portability| Supported across compatible hypervisors| Supported across compatible container runtimes
  Docker;
Docker is a platform for building, distributing and running containers.
  Important concepts:
- Image: A template used to create containers.
- Container: A running instance of an image.
- Dockerfile: Instructions for building an image.
- Docker Registry: A repository for storing and distributing images.
- Volume: Persistent storage used by containers.
- Network: Enables communication between containers and external systems.
  Kubernetes;
Kubernetes is a container orchestration platform used to deploy, scale and manage containerised applications.
Important concepts:
- Pod: Smallest deployable unit in Kubernetes.
- Node: Machine that runs workloads.
- Cluster: Collection of control-plane and worker resources.
- Deployment: Defines and manages application replicas.
- Service: Provides stable network access to application pods.
- ConfigMap: Stores non-sensitive configuration.
- Secret: Stores sensitive configuration data.
Applications: Microservices, scalable web applications and distributed software systems.

 Cloud Storage Systems
Cloud storage allows users and applications to store and retrieve data through network-accessible infrastructure.
  Object Storage;
Stores data as objects containing the data itself, metadata and a unique identifier.
Examples:
- Amazon S3.
- Azure Blob Storage.
- Google Cloud Storage.
Applications:
- Images and videos.
- Backups.
- Data lakes.
- Large unstructured datasets.
  Block Storage;
Stores data in fixed-sized blocks that can be attached to virtual machines or servers as storage volumes.
Applications:
- Operating system disks.
- Virtual machine storage.
- High-performance databases.
  File Storage;
Stores data in files organised into directories and folders.
Applications:
- Shared documents.
- Enterprise file systems.
- Network-attached storage.
Comparison
Storage type| Organisation| Common use
Object| Objects with metadata| Media, backups, data lakes
Block| Fixed-sized blocks| VM disks, databases
File| Files and directories| Shared files and applications
  Important storage considerations;
- Capacity.
- Performance and latency.
- Durability.
- Availability.
- Replication.
- Backup and recovery.
- Access permissions.
- Storage cost.

 Cloud Networking
Cloud networking connects virtual machines, storage, applications and external users.
  Important components;
1. Virtual Private Cloud (VPC): A logically isolated virtual network within a public cloud.
2. Subnets: Divide a network into smaller address ranges.
3. Virtual Network Interfaces: Connect virtual machines to networks.
4. Routers: Forward packets between networks.
5. Security Groups: Control permitted network traffic to and from resources.
6. Network Access Control Lists (NACLs): Apply network-level traffic rules to subnets in platforms that support them.
7. Load Balancers: Distribute incoming traffic across multiple servers.
8. VPN: Establishes an encrypted connection over an untrusted network.
9. DNS: Translates domain names into IP addresses.
  Load balancing;
Load balancing distributes incoming requests among available servers to improve performance and availability.
A simple average-load calculation is:
    L_{average}={Total incoming workload}/{Number of active servers}
Actual distribution depends on the load-balancing algorithm.
  Common algorithms:;
- Round robin.
- Weighted round robin.
- Least connections.
- IP hash.
- Least response time.

 Cloud Computing and Scalability
Scalability is the ability of a system to handle increasing workloads by allocating additional resources.
  Vertical Scaling (Scale Up);
Increasing the resources of an existing server.
Examples:
- More CPU cores.
- More RAM.
- Faster storage.
Advantages:
- Simple to implement.
- May require fewer application changes.
Limitations:
- Hardware limits.
- Can require downtime.
- May create a single point of failure.
  Horizontal Scaling (Scale Out);
Adding more servers or computing instances to distribute workloads.
Advantages:
- Supports large workloads.
- Improves fault tolerance.
- Can provide greater flexibility.
Limitations:
- Requires distributed-system design.
- May introduce coordination and data-consistency challenges.
  Elasticity;
Elasticity is the ability to automatically or dynamically increase and decrease resources according to demand.
Example: An online shopping application automatically adds servers during high-traffic periods and removes them when demand falls.

 Cloud Computing Models for Applications
  Serverless Computing;
Allows developers to run code without directly managing servers.
The cloud provider manages the infrastructure and automatically provisions resources.
Examples:
- AWS Lambda.
- Azure Functions.
- Google Cloud Run functions.
Advantages:
- Reduced infrastructure management.
- Automatic scaling.
- Usage-based billing.
- Suitable for event-driven workloads.
Limitations:
- Execution limits may apply.
- Cold-start latency can occur.
- Platform dependence.
- Not ideal for every continuously running workload.
  Microservices Architecture;
An application is divided into small, independent services that communicate through APIs or messaging systems.
Example: An online store may have separate services for:
- User authentication.
- Product catalogues.
- Payments.
- Orders.
- Inventory.
Advantages:
- Independent deployment.
- Independent scaling.
- Easier development by separate teams.
- Fault isolation when properly designed.
Challenges:
- Distributed communication.
- Service monitoring.
- Data consistency.
- Increased operational complexity.
  API-Based Integration;
An Application Programming Interface (API) allows different software systems to communicate.
Common approaches:
- REST APIs.
- GraphQL.
- gRPC.
- WebSockets.
APIs enable cloud applications to integrate with mobile applications, databases, IoT systems and external services.

 Cloud Computing and Data Processing
Cloud infrastructure provides scalable environments for processing large volumes of data.
  Common processing approaches;
Batch processing: Processes accumulated data at scheduled intervals.
Example: Generating daily sales reports.
Stream processing: Processes data continuously as it arrives.
Example: Analysing live sensor measurements.
Distributed processing: Divides large computational tasks across multiple machines.
Examples:
- Apache Spark.
- Apache Flink.
- Hadoop.
  Data lake;
A centralised repository that stores large volumes of raw data in different formats.
  Data warehouse;
A system designed to store structured, organised data for reporting and analytical queries.
  ETL and ELT;
- ETL: Extract, Transform, Load.
- ELT: Extract, Load, Transform.
These processes move data from source systems into storage and analytical environments.

 Cloud Security
Cloud security involves protecting cloud infrastructure, applications, identities and data from unauthorised access, attacks and failures.
  Shared Responsibility Model;
Cloud security responsibilities are divided between the cloud provider and customer.
The provider generally secures the underlying cloud infrastructure, while customers remain responsible for securing their data, identities, access configurations and workloads according to the service model.
The exact division varies between IaaS, PaaS and SaaS.
  Common security threats;
- Data breaches.
- Misconfigured storage.
- Weak passwords.
- Account hijacking.
- Malware and ransomware.
- Denial-of-Service attacks.
- Insecure APIs.
- Insider threats.
- Unpatched software.
  Security measures;
1. Identity and Access Management (IAM): Controls who can access cloud resources.
2. Multi-Factor Authentication (MFA): Requires multiple forms of authentication.
3. Encryption: Protects data in transit and at rest.
4. Firewalls: Filter network traffic.
5. Least privilege: Grants only the permissions required for a task.
6. Key management: Protects and controls encryption keys.
7. Monitoring and logging: Detects suspicious activity.
8. Backup and recovery: Protects against data loss.
9. Security patching: Fixes known vulnerabilities.
10. Network segmentation: Separates systems to limit unauthorised access and attack propagation.

 Cloud Availability and Disaster Recovery
Cloud systems should be designed to remain operational during hardware failures, network problems and other disruptions.
  Important concepts;
Availability: The percentage of time a service is operational.
    A=MTBF/MTBF+MTTR
Where:
- MTBF = Mean Time Between Failures.
- MTTR = Mean Time To Repair.
Percentage availability:
    A(%)=MTBF/MTBF+MTTR*100
Fault tolerance: The ability of a system to continue operating despite component failures.
Redundancy: Providing duplicate resources to reduce the risk of service interruption.
Replication: Maintaining copies of data or services across multiple systems or locations.
  Disaster recovery metrics;
Recovery Time Objective (RTO): Maximum acceptable time required to restore a service after a disruption.
Recovery Point Objective (RPO): Maximum acceptable amount of data loss measured in time.
Example:
- RTO = 2 hours.
- RPO = 15 minutes.
This means the service should be restored within two hours, and the recovery strategy should limit data loss to approximately 15 minutes of updates.
  Disaster recovery strategies;
- Regular backups.
- Data replication.
- Multi-zone deployment.
- Cross-region recovery.
- Automated failover.
- Disaster recovery testing.

 Cloud Monitoring and Management
Cloud resources must be monitored to ensure performance, availability, security and cost efficiency.
  Key monitoring metrics;
- CPU utilisation.
- Memory usage.
- Disk usage.
- Network bandwidth.
- Application response time.
- Request rate.
- Error rate.
- Service availability.
- Storage consumption.
- Cloud expenditure.
  Common tools;
- Amazon CloudWatch.
- Azure Monitor.
- Google Cloud Monitoring.
- Prometheus.
- Grafana.
- OpenTelemetry.
  Infrastructure as Code (IaC);
Infrastructure as Code is the practice of defining and managing infrastructure through machine-readable configuration files rather than manual configuration.
Examples:
- Terraform.
- AWS CloudFormation.
- Ansible.
Advantages:
- Repeatable deployments.
- Version control.
- Automation.
- Reduced configuration errors.
- Easier infrastructure recovery.

 Cloud Cost Management
Cloud services commonly use pay-as-you-go pricing, where users pay according to resource consumption.
  Common cost factors;
- Compute instance usage.
- Storage capacity.
- Data transfer.
- Database operations.
- API requests.
- Backup and monitoring services.
- Software licensing.
  Cost optimisation techniques;
- Shut down unused resources.
- Select appropriate instance sizes.
- Use autoscaling.
- Apply storage lifecycle policies.
- Monitor network data-transfer charges.
- Use reserved or committed-use pricing where suitable.
- Set budgets and billing alerts.
- Review resource utilisation regularly.
Important: 
Cloud computing can reduce upfront hardware investment, but poor resource management can result in unexpectedly high operating costs.

 Practical Cloud Computing Workflow
A typical cloud deployment follows these steps:
1. Define the application and infrastructure requirements.
2. Select a suitable cloud provider.
3. Choose a deployment model.
4. Select appropriate IaaS, PaaS or SaaS services.
5. Design the virtual network and security boundaries.
6. Provision computing and storage resources.
7. Configure operating systems, applications and databases.
8. Deploy applications using suitable tools.
9. Configure access control and encryption.
10. Set up monitoring, logging and alerts.
11. Configure backups and disaster recovery.
12. Test performance, availability and security.
13. Monitor usage and optimise costs.
  Practical tools to learn;
Area| Tools / Technologies
Cloud platforms| AWS, Azure, Google Cloud
Virtualisation| VMware, Hyper-V, KVM
Containers| Docker
Orchestration| Kubernetes
Infrastructure as Code| Terraform
Configuration management| Ansible
CI/CD| GitHub Actions
Monitoring| Prometheus, Grafana
Data processing| Apache Spark
Operating systems| Linux, Ubuntu
Networking| TCP/IP, DNS, VPN, VPC

 Important Engineering Design Considerations
When designing cloud infrastructure, consider:
- Scalability: Can the infrastructure handle increasing demand?
- Availability: Can services remain accessible?
- Reliability: Can workloads recover from failures?
- Security: Are identities, applications and data protected?
- Performance: Are computing and network resources sufficient?
- Cost: Is the infrastructure financially sustainable?
- Portability: Can workloads move between environments?
- Interoperability: Can different services communicate?
- Maintainability: Can the system be updated and managed efficiently?
- Compliance: Does the system meet applicable legal and regulatory requirements?
  Key Engineering Tips;
- Understand networking before designing complex cloud architectures.
- Learn Linux and virtualisation fundamentals.
- Understand the difference between VMs and containers.
- Use IAM and least-privilege access from the beginning.
- Automate infrastructure using IaC.
- Monitor resource usage and costs continuously.
- Design backups and disaster recovery before deployment.
- Avoid unnecessary complexity in small systems.
- Use horizontal scaling when workloads and application architecture support it.
- Understand the shared responsibility model before deploying sensitive applications.

 Summary
Cloud computing provides on-demand access to computing, storage, networking and software resources through network-accessible infrastructure.
Its main components include physical data centres, virtualisation, containers, cloud networks, storage systems, computing platforms, applications, security and management services.
The main service models are IaaS, PaaS and SaaS, while the major deployment models are public, private, hybrid and community cloud.
  A typical cloud application operates through:
User → Internet → Cloud Network → Compute Resources → Application / Database / Storage → Response to User.
The central engineering principle is to design cloud infrastructure that is scalable, secure, reliable, cost-effective and maintainable.