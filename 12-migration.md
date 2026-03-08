# Migration
## Three Phases of the Migration Process
- Assess
  - In this phase, you build the business case for the migration and assess your readiness. One of the services used in this phase is the Migration Evaluator.
- Mobilize
  - In this phase, you prepare the organization and mobilize the resources needed for the migration. Two services you might use in this phase are AWS Application Discovery Service and the AWS Migration Hub.
- Migrate and Modernize
  - In this phase, you use your strategy, plan, and the best practices to migrate and modernize. Tools to support you include AWS Application Migration Service and AWS Database Migration Service (AWS DMS). If you are transferring data, you might use AWS DataSync, AWS Transfer Family, and the AWS Snow Family.

## AWS CAF
- A framework that brings AWS experience and best practices to companies preparing to migrate to the AWS Cloud.
- Provides benefits for migrations to reduce business risk and improve sustainability and corporate transparency.
- You can use AWS CAF to migrate technology like legacy infrastructure and applications. You can also use it to migrate and optimize business processes, operations, and even create new business models with the move to the cloud.

### The Perspectives
Here are some of the perspectives to consider when migrating:
- Business
  - Makes sure that IT aligns with business needs and that IT investments link to key business results.
  - Use the Business perspective to create a strong business case for cloud adoption and prioritize cloud adoption initiatives. Make sure that your business strategies and goals align with your IT strategies and goals.
  - Roles for this are:
    - Business managers
    - Finance managers
    - Budget owners
    - Strategy stakeholders
- People
  - Supports development of an organization-wide change management strategy for successful cloud adoption.
  - Use the People perspective to evaluate organizational structures and roles, assess new skill and process requirements, and identify gaps. This helps prioritize training, staffing, and organizational changes.
  - Roles for this are:
    - Human resources
    - Staffing
    - People managers
- Governance
  -  Focuses on skills and processes to align IT strategy with business strategy. This perspective helps you maximize business value and minimize risks.
  -  Use it to understand how to update the staff skills and processes necessary to maintain business governance in the cloud. Manage and measure cloud investments to evaluate business outcomes.
  - Roles for this are:
    -  Chief Information Officer (CIO)
    -  Program managers
    -  Enterprise architects
    -  Business analysts
    -  Portfolio managers
- Platform
  - Includes principles and patterns for implementing new solutions in the cloud and migrating on-premises workloads to the cloud.
  - Use a variety of architectural models to understand and communicate the structure of IT systems and their relationships. Describe the architecture of the target state environment in detail.
  - Roles for this are:
    - Chief Technology Officer (CTO)
    - IT managers
    - Solutions architects
  - Security
    - Makes sure that the organization meets security objectives for visibility, auditability, control, and agility.
    - Use AWS CAF to structure the selection and implementation of security controls that meet the organization’s needs.
    - Roles for this are:
      - Chief Information Security Officer (CISO)
      - IT Security Managers
      - IT Security Analysts
- Operations
  - Helps you to enable, run, use, operate, and recover IT workloads to the level agreed upon with your business stakeholders.
  - Define how day-to-day, quarter-to-quarter, and year-to-year business is conducted. Align with and support the operations of the business. AWS CAF helps these stakeholders define current operating procedures and identify the process changes and training needed to implement successful cloud adoption.
  - Roles for this are:
    - IT Operations Managers
    - IT Support Managers

## The 7 Rs
1. Relocate - changing the hosting location to the cloud.
2. Rehost - aka lift and shift. Move apps without changes.
3. Replatform - aka lift, tinker, and shift. Make a few cloud optimizations, this is achieved without changing the core architecture of the app.
4. Refactor - aka re-architecting. Reimagining how the app is developed by using built features for the cloud. Done when adding features, scaling, and/or improving performance would be difficult to be done in the app's current environment.
5. Repurchase - moving from a traditional to SaaS model.
6. Retain - Keeping applications that are critical for the business in the source environment. 
7. Retire - Removing applications that are no longer needed.

# Migration Services and Tools
## Migration Evaluator (Assess Phase)
- A migration assessment service that helps you create a business case for AWS Cloud planning and migration. It does this with a data driven approach, analyzing your current state, target state, and developing a migration readiness plan with projected cloud costs.
- Removes the guesswork when migrating, provides visibility into multiple cost-effective cloud migration scenarios, and also gives insights on reusing existing software licensing, which can reduce costs.
- You can use Migration Evaluator to conduct broad-based discovery, take a snapshot of your current on-premises footprint to fine-tune licensing, view server dependencies, and gain visibility into multiple migration scenarios. You can also use it to estimate and reduce your cloud costs.

## Application Discovery Service (Mobilize Phase)
- Discovers on-premises server inventory and connections. It gathers configuration, performance, and connection details for both servers and databases to create a detailed migration plan.
- Get a comprehensive snapshot of your on-premises inventory. You also can integrate discovery data with other services like Migration Hub and protect the data Application Discovery Service collects.

## Migration Hub
- A centralized hub to take you from discovery, assessment, planning, and execution of your migration. It provides tools, guidance, and automated recommendations to collaborate with your team and track your migration.
- With the Migration Hub, you have one location to go for your migration and, expert guidance in the form of prescriptive journey templates.
- You can use Migration Hub for migration assessment and planning and migration completion and collaboration with teams.

## Application Migration Service (Migrate and Modernize Phase)
- It is a tool to move and improve your on-premises and cloud-based applications since it makes it possible to modernize your applications during migration. You can maintain normal business operations during the application replication process and also reduce costs by using one tool for a wide range of applications.
- You can use the Application Migration Service for on-premises applications running on physical servers or infrastructure, cloud-based applications, or moving between AWS Regions. You can also use it to modernize applications.

# Migrating Databases
## AWS DMS
- The AWS Database Migration Service (AWS DMS) makes it possible to quickly and securely migrate databases and perform ongoing data replication tasks for live databases and data warehouses.
- It supports homogenous and heterogenous migrations. It also makes it possible to migrate terabyte sized databases at a low cost.
- You can use AWS DMS to move to managed databases, remove licensing costs, replicate ongoing changes in your database, and improve integration with data lakes.

## AWS SCT
- The AWS Schema Conversion Tool makes it possible to convert database schemas and code objects (like stored procedures, views, and functions) from one database engine to another.
- Simplify database migrations by automating schema analysis, recommendations, and conversion at scale.
- Compatible with popular databases and analytics services as source and target engines. It can save weeks or months of manual time and resources, which are typically required in conversions.
- You can use AWS SCT to move from commercial databases to open source databases.

# Transferring Data Online
## AWS DataSync
- Designed for automating and accelerating data transfer.
- Accelerates moving large amounts of data between on-premises storage and AWS storage services like Amazon S3.
- DataSync manages data movement workloads with bandwidth throttling, migration scheduling, task filtering, and task reporting.
- Provides data replication.
- You can use DataSync to migrate your data, archive your cold data, and manage hybrid data workflows.

## AWS Transfer Family
- Provides fully managed support for secure file transfers over FTP, Secure File Transfer Protocol (SFTP), File Transfer Protocol Secure (FTPS), and other protocols.
- The Transfer Family provides secure data transfer with encryption and authentication, to ensure data integrity and confidentiality. It is built to scale and streamline workflows.
- You can use the Transfer Family to modernize and manage your file transfers, simplify data sharing with your workforce and partners, and integrate transactional business data into a unified data lake.

## Direct Connect
- A service that makes it possible for you to establish a dedicated private connection between your network and virtual private cloud (VPC) in the AWS Cloud. Helping reduce the network costs and increase amount of bandwidth.

# Transferring Data Offline
## Snowball Edge Storage Optimized devices
- These devices deliver high performance NVMe storage, making it possible to simplify multi-petabyte data migrations from on-premises locations to AWS.
- Better compute performance and larger storage capacity with gigabytes of data per second for data migration workloads with offline requirements.
- You can use Snowball Edge devices for data migration when offline migration is required. They can also be used for edge computing when a secure, rugged device is needed.
