# Block Storage
## Amazon EC2 Instance Store
- Block-level storage that is physically attached to the EC2 instance host computer.
- Best for temporary memory-based storage since its data is lost when an instance is stopped or terminated.
- Buffers, caches, and scratch data

Benefits:<br>
- Automatically available storage<br>
- Cost effective<br>
- High I/O performance<br>

## Amazon Elastic Block Store (EBS)
- Provides persistent block-level storage volumes for use with Amazon EC2 instances.
- Consistent and low-latency performance for workloads like databases and file systems.
- After the EC2 instance is stopped or terminated, all data stored within the EBS volume is retained.
- Provides high availability and durability by automatically replicating volumes within the same Availability Zone.
- EBS volumes exist independently from the instance and persist even after the instance is terminated.

Benefits:<br>
- Data migration<br>
- Disaster Recovery<br>
- Cost optimization/modification<br>
- Performance tuning<br>

## EBS Snapshots
- Point-in-time backups of EBS volumes.
- Used for disaster recovery, data migration, volume resizing, and for creating consistent backups of production workloads. 
- Customer is responsible for scheduling and managing regular EBS snapshots as part of their backup strategy. 

Benefits:<br>
- Data protection and recovery<br>
- Operational Flexibility<br>
- Cost effective<br>

## Amazon Data Lifecycle Manager Workflow
- Helps maintain compliance requirements by scheduling regular backups and enforcing retention rules.

Steps:
1. Create an EBS snapshots policy using the Amazon EC2 console, API calls, AWS Command Line Interface (AWS CLI), SDKs, or AWS CloudFormation.
2. Choose either an EBS volume or an EC2 instance as the target for the snapshot.
3. Narrow down the data to be included in the snapshot by choosing options to exclude either the root volume or data volumes.
4. Automate the creation, retention, and deletion of EBS snapshots by setting up custom schedules.
5. You can apply additional actions like tags, snapshot archiving, Amazon EBS fast snapshot restore, cross-Region copying, and cross-account sharing.

# Object Storage
## Amazon Simple Storage Service (S3)
- A fully managed, highly-available object storage service for storing and retrieving any amount of data as objects.
- Stores files as objects in containers known as buckets, and each object can range in size from a few bytes to several terabytes.
- Uploading a file to S3 turns it to an object and is stored durably across multiple facilities within your chosen Region.

## S3 Objects
- Includes the data itself, metadata, and a unique identifier, or key.
- Can be of any file type, such as images, videos, documents, or application data, and can range in size from a few bytes to several terabytes.
- Uniquely identified within a bucket by its key.

## S3 Buckets
- Container for storing objects in Amazon S3. 

Benefits:<br>
- No fixed storage limit, scaling automatically to accommodate any amount of data you need.<br>
- Automatically moves objects between storage classes based on your defined rules.<br>
- Supports a wide range of use cases for both cloud-based applications and traditional on-premises workloads.<br>

## Storage Classes
- <b>S3 Standard:</b> Considered general-purpose storage for cloud applications, dynamic websites, content distribution, mobile and gaming applications, and big data analytics.

- <b>S3 Intelligent-Tiering:</b> Stores objects in three tiers: a frequent access tier, an infrequent access tier, and an archive instant access tier. It monitors access patterns of your data and automatically moves your data to the most cost-effective storage tier based on frequency of access.

- <b>S3 Standard Infrequent Access (Standard-IA):</b> For data that is accessed less frequently but requires rapid access when needed. 

- <b>S3 One Zone Infrequent Access (One Zone-IA):</b> Stores data in a single Availability Zone, reducing costs compared to S3 Standard-IA, which uses three zones. 

- <b>S3 Express One Zone:</b> Stores data in a single Availability Zone. It was purpose-built to deliver consistent single-digit millisecond data access for your most frequently accessed data and latency-sensitive applications.

- <b>S3 Glacier Instant Retrieval:</b> For archiving data that is rarely accessed and requires millisecond retrieval. 

- <b>S3 Glacier Flexible Retrieval:</b> For archived data that is accessed 1–2 times per year. Your data can be accessed in as little as 1–5 minutes using an expedited retrieval. 

- <b>S3 Glacier Deep Archive:</b> Lowest-cost Amazon S3 storage class. Supports long-term retention and digital preservation for data that might be accessed once or twice per year. 

- <b>S3 Outposts:</b> Delivers object storage to your on-premises AWS Outposts environment using Amazon S3 APIs and features, and serves workloads with local data residency requirements.

<b>To avoid manually managing your object storage tier configurations, you can use S3 Lifecycle configurations to automate the process.</b>

# File Storage
## Amazon Elastic File System (EFS)
- Fully managed, scalable file storage service for use with AWS cloud services and on-premises resources.
- Operates using the Linux Network File System (NFS) protocol.
- Automatically replicates data across multiple AZs in a region for high availability.
- Multiple EC2 instances can access the same file system simultaneously. 
- Automatically grows and shrinks as you add and remove files.

## EFS Storage Classes
- EFS Standard and EFS Standard-Infrequent Access (Standard-IA) storage classes offer Multi-AZ resilience and the highest levels of durability and availability. They have a higher cost associated with them due to higher availability and durability.
- EFS One Zone and EFS One Zone-Infrequent Access (EFS One Zone-IA) provide additional savings by saving your data in a single Availability Zone. By using just one Availability Zone, you can reduce your storage costs when compared to the Standard EFS storage classes.
- EFS Archive storage class is cost-optimized for data that is accessed only a few times a year or less and that does not need the sub-millisecond latencies of EFS Standard. EFS Archive offers a storage price up to 50% lower compared to EFS Infrequent Access, providing a more cost-optimized experience for cold, rarely-accessed data.

## Amazon FSx
- Fully managed service that supports multiple filesystem protocols compared to Amazon EFS, this includes Windows File Server, Lustre, OpenZFS, and NetAPP ONTAP.
- Built on latest AWS compute to provide high performance and low total cost of ownership.
- Supports industry-standard file system protocols, allowing convenient integration.
- Reduces the complexity of managing infrastructure while delivering the features and capabilities of traditional file systems.
- It has scalable storage.

## Amazon FSx for Windows
- Migrates Windows file servers to AWS.
- Accelerate hybrid workloads.
- Reduce SQL Server deployment cost.

## Amazon FSx for NetApp ONTAP
- Migrates workloads to AWS seamlessly.
- Modernizes the data management.
- Streamline business continuity.

## Amazon FSx for OpenZFS
- Deliver insights  faster for data analytics workloads.
- Accelerate content management.
- Increase dev/test velocity.

## Amazon FSx for Lustre
- Accelerate machine learning (ML).
- Enable high performance computing.
- Increase media workload agility.

# Additional Storage Solutions
## AWS Storage Gateway
- Hybrid cloud storage service used to extend local storage to cloud while maintaining low-latency access to frequently used data.
- Provides smooth connectivity between on-premise and AWS Cloud storage, which allows for improved data management.
- Locally keeps frequently accessed data for quick access.

## Gateway Types
- <b>Amazon S3 File Gateway:</b> Bridges local environment with Amazon S3. Providing virtually unlimited cloud storage to on-premises applications through familiar file protocols.
- <b>Volume Gateway:</b> Uses virtual storage volumes while maintaning local access. It functions as a bridge between on-premises and AWS Cloud storage by presenting data as iSCSI volumes that can be mounted by the existing app.
  - Cached volume mode stores primary data in the cloud while frequently accessed data is cached locally for low-latency access.
  - Stored volume mode locally keeps your complete dataset while asynchronously backing it up to the cloud as EBS snapshots.
- <b>Tape Gateway:</b> Makes it possible to replace physical tape infrastructure with virtual tape capabilities while benefitting from the durability and scalability of AWS Cloud storage. <b>Designed for archiving not frequent file access.</b>

## AWS Elastic Disaster Recovery
- Replicates critical workloads to AWS with minimal downtime.
- Supports both physical and virtual servers to enable rapid recovery during disruptions.
- The servers' block-level data is continuously replicated to AWS.

## Use cases
- <b>Healthcare data protection:</b> Maintains compliance while protecting patient records by replicating on-premises servers to AWS.
- <b>Financial services continuity:</b> Protects their core banking applications by continuously replicating their transaction processing systems.
- <b>Manufacturing operations recovery:</b> Employs Elastic Disaster Recovery to protect their production planning systems.

## Cloud in Real Life
- S3 is used for static website hosting by uploading HTML, CSS, JavaScript, and media files to a bucket and enabling static hosting.
- EBS is the perfect solution for databases that require fast, consistent read/write operations and block-level storage.
- EFS is best for shared file systems requiring simultaneous access across multiple instances.
