## Authentication
- The process of verifying the identity of a user or entity through credentials like a username and password combination.
  - An employee logs in to an employee portal.

## Authorization
- Grants users certain access rights and permissions that determine which actions they can perform in a system or application.
  - An employee can access their own records, but they're not allowed to access other employee's records.

## Shared Responsibility in Security
- Customers are responsible for:
  - Managing the security of data, systems, and applications.
  - Deciding what data and workloads to store or run in AWS.
  - Determining which AWS service to use.
  - Controlling who has access to certain environments.

- AWS is responsible for:
  - The foundational software that powers AWS service.
  - The virtualization layer.
  - The hardware and global infrastructure that supports the data centers from which services operate. This includes protection for AWS Regions, Availability Zones, and edge locations.

## AWS security controls
AWS offers the following security mechanisms:
- Prevents security incidents through proper permission and access management.
- Protects networks, applications, and data.
- Detect and respond to security incidents as they occur.

## AWS Identity and Access Management (IAM)
- By default, all actions are denied. Users must explicitly grant permission to someone before they can perform any actions in your account.
- Principle of least privilege is when you provide access only on a need-to-have basis.

## Additional Access Management Servies
1. AWS IAM Identity Center
   - Centralizes identity and access management across AWS accounts and applications. IAM Identity Center can also connect to an existing identity source and provide your workforce with single sign-on access to all your connected AWS services and accounts. This is called federated identity management.
     
2. AWS Secrets Manager
   - Provides a secure way to manage, rotate, and retrieve database credentials, API keys, and other secrets throughout their lifecycle. This helps keep your applications, services, and IT resources safe.
     
3. AWS Systems Manager
   - Provides a centralized view of nodes across your organization’s accounts and Regions and multi-cloud and hybrid environments. With this service, you can quickly access node information, such as ID and operating system details, and automate registry edits, user management, and security patching.
  
## Network and Application Attacks
- <b>DoS Attacks:</b> An attacker floods a web application with excessive network traffic. Legitimate customer requests are denied if the web application becomes overloaded and can no longer respond.
- <b>DDoS Attacks:</b> An attacker can use multiple infected computers (called zombie bots) to unknowingly send excessive traffic to a web application.

<b>DoS uses one machine/connection, making it easier to mitigate, while DDoS uses multiple, often global, sources (botnets) to launch massive, harder-to-stop attacks. </b>

## AWS Network and Application Protection
AWS automatically protects against low-level, brute-force attacks, such as DDoS, through its built-in infrastructure and network architecture.

- Security groups only allow in proper request traffic. They operate at the AWS network level so they can shrug off massive attacks using the entire AWS Region's capacity.
- ELB handles traffic first before handing it off, so your frontend server is not overwhelmed. It runs at the Region level.
- The enormous capacity of Regions makes them extremely difficult to overwhelm. It would be massively expensive to achieve.

# AWS Protection through Services
## AWS Shield
- <b>Standard:</b> Designed to automatically protect AWS customers from the most common, frequently occurring types of DDoS attacks at no cost. It uses a variety of analysis techniques to detect and mitigate incoming malicious network traffic in real time.
- <b>Advanced:</b> A paid service that provides detailed attack diagnostics and the ability to detect and mitigate sophisticated DDoS attacks. It also integrates with other services, such as Amazon CloudFront, Amazon Route 53, and ELB.

## AWS WAF
- A web application firewall that monitors network requests that come into your web applications. When a request comes into AWS WAF, it checks the IP address against a web access control list (web ACL). If the request comes from a blocked IP address on the web ACL, AWS WAF denies access. Legitimate requests are allowed access.

## Data Encryption
- Works like a lock and key mechanism. Having the right key can access the encrypted data. Otherwise, you cannot access the data.
- An encryption key is used to turn the profile information into a randomized set of characters. A decryption key is used to access the customer's information, such as their name, only when it's needed by your application.

Types:
1. Data encryption at rest: The data is idle and not moving, like when it's stored in a database.

2. Data encryption in transit: The data is moving between locations, like when it's being sent from a database to an application. SSL/TLS certificates are used to establish encrypted network connections from one system to another.

# AWS Data Protection
AWS has a variety of methods for protecting data. They include built-in data protection for storage options and services specifically designed for enhanced data protection.

## AWS built-in data protection
- By default, all new S3 buckets have encryption configured, and all uploaded objects are encrypted at rest.
- Amazon EBS volumes and snapshots can be encrypted at rest, including both boot and data volumes of an Amazon EC2 instance.
- Server-side encryption at rest is enabled on all DynamoDB table data using encryption keys stored in AWS Key Management Service (AWS KMS).

# AWS Data Protection Services
## AWS Key Management Service (AWS KMS)
-  Create and manage cryptographic keys. These keys can then be used to encrypt and decrypt your data. You can also control the use of keys across a wide range of services and in your applications.
-  You can specify which IAM users and roles can manage keys. Your keys never leave AWS KMS, and you can temporarily disable them so they can no longer be used.

## Amazon Macie
- Monitor your sensitive data at rest to make sure it's safe. Macie uses machine learning (ML) and automation to discover sensitive data stored in Amazon S3. You can use Macie to assess your security posture, which is especially helpful for meeting compliance requirements.

## AWS Certificate Manager (ACM)
- Centralizes the management of your SSL/TLS certificates that provide data encryption in transit (data that is moving). It can be used to protect various AWS services and your connected on-premises resources.

# Detection and Response Services
AWS offers a variety of services you can use to detect and respond to security incidents.

## Amazon Inspector
-  Helps improve the security and compliance of applications by running automated security assessments for Amazon EC2 instances, containers, and Lambda functions.
-  It checks applications for security vulnerabilities and deviations from security best practices, such as open access to EC2 instances and installations of vulnerable software versions.

## Amazon GuardDuty
- Provides intelligent threat detection across your infrastructure and resources. GuardDuty identifies threats by continuously monitoring streams of your account metadata and network activity in your environment.
- It uses known malicious IP addresses, anomaly detection, and machine learning to identify threats more accurately.

## Amazon Detective
- After a threat has been detected, you can use Amazon Detective to further investigate the root cause. Detective helps you analyze threats with interactive visualizations contained in a unified AWS Management Console view.
- These visualizations include resource and user interactions over a configurable timeline with recommended steps for remediation.

AWS Security Hub
- Brings multiple security services together into a single place and format. With this service, you can quickly see your security and compliance state in one comprehensive view.
- Security Hub automatically aggregates security findings from AWS and partner services and organizes them into actionable, meaningful groupings called insights. It can accelerate time to resolution (TTR) with automated remediation.
