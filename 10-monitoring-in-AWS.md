## Monitoring your resources in the AWS Cloud
The general progression is as follows:
1. Securing systems
2. Monitoring activities
3. Conducting audits
4. Ensuring compliance

## Importance of Monitoring
1. Maintain Security
2. Respond Proactively
3. Ensure Reliability
4. Monitor Costs
5. Improve Performance

## Amazon CloudWatch
- Monitors your AWS resources and the applications that you run on AWS in real time.
- With CloudWatch, you gain system-wide visibility into resource utilization, application performance, and operational health.
- Other features:
  - CloudWatch metrics: Monitor the metrics from your AWS resources.
  - CloudWatch alarms: Set a threshold to configure an automatic notifcation sender or changes in resources.
  - CloudWatch dashboards: Customizable home pages where you can use to monitor everything in a singe page.
  - CloudWatch logs: centralizes the logs from all of the systems, and AWS services that you use.

## Auditing
Frequent changes are prone to human error, and if one happens it is important to figure out what happened when there are changes made to the resources in the cloud or on premises. This information is needed for troubleshooting and to provide detailed records for compliance. 

## AWS CloudTrail
- Tracks user activity and API usage in the AWS Cloud, on premises, and even with other cloud providers. It provides a detailed history of API calls, so you can track changes and identify who made them and when.
- It can be used for compliance and auditing, identifying security incidents, troubleshooting operational issues.
  - CloudTrail events: Captures details about actions performed within your AWS account, such as API calls, console actions, or other activities.
  - CloudTrail logs: Monitors events and delivers those events as log files to your Amazon Simple Storage Service (Amazon S3) bucket.
  - CloudTrail Insights: Analyzes your normal patterns of API call volume and API error rates. It can detect anomalous behavior and unusual activity, generating Insights events when API call volumes and error rates deviate from these normal patterns.

## AWS Artifact
- A service that provides no-cost, on-demand access to AWS security and compliance reports and select online agreements.
- AWS Artifact helps you manage at scale, save time with on-demand access to compliance reports, and deploy with more confidence. It can be used to manage select online agreements and assess third-party security and compliance.
- Consists of two types:
  - AWS Artifact Agreements: You can review, accept, and manage agreements for an individual account and for all your accounts in AWS Organizations.
  - AWS Artifact Reports: Provides compliance reports from third-party auditors. These auditors have tested and verified that AWS is compliant with a variety of global, regional, and industry-specific security standards and regulations.

## AWS Compliance Portal
- Contains resources to help you learn more about AWS compliance. You can read customer compliance stories to discover how companies in regulated industries have solved various compliance, governance, and audit challenges.

## AWS Config
- A service that you can use to assess, audit, and evaluate the configurations of your AWS resources. Focuses on WHAT happened in comparison to AWS Cloudtrail which focuses on WHO.

## AWS Organizations
- Helps you centrally manage and govern your environment as you grow and scale your AWS resources.
- Provides several benefits like quickly scaling your environment by programmatically creating new AWS accounts for resources and teams. It also helps by simplifying permission management through SCPs and managing and optimizing costs across your AWS accounts and resources.

# Governance in the AWS Cloud
## AWS Control Tower
A service you can use to enforce and manage governance rules for security, operations, and compliance at scale across all your organizations and accounts in the AWS Cloud.
- Benefits: AWS Control Tower can help you save time while providing governance. It uses preconfigured controls, which can help you to quickly set up multi-account environments, automation with built-in governance, and integration of third-party software at scale.
- Use cases: Use AWS Control Tower to quickly deploy applications and provision compliant AWS accounts.

## AWS Service Catalog
You can create, share, and organize from a curated catalog of AWS resources. You can deploy baseline networking resources and security tools for new AWS accounts so you can govern consistently.
- Benefits: Service Catalog saves time by making it quick to find and deploy approved, self-service cloud resources. It also helps you stay agile while improving governance over resources across multiple accounts
- Use cases: Use it to provision resources across AWS accounts, apply access controls, and accelerate provisioning of continuous integration and continuous delivery (CI/CD) pipelines.

## AWS License Manager
A service that helps you manage your software licenses and fine-tune your licensing costs. It helps reduce the risk of noncompliance by enforcing license usage limits, blocking new launches, and using other controls.

- Benefits: License Manager helps with visibility and control, tracking and managing licenses, and reducing the risk of noncompliance with licenses.
- Use cases: Use it to streamline license management and to simplify the Microsoft License Mobility through Software Assurance experience. You can also use it to automate the distribution and activation of software entitlements across AWS accounts for end users.

#
## AWS Health Dashboard
With AWS Health Dashboard, you can view account-specific health information and get AWS Health event updates. You can also use AWS Health programmatically using the AWS Health API, which is available with AWS Premium Support.
- Benefits: AWS Health Dashboard provides valuable information as a data source for events and changes. It gives you timely and actionable guidance to remedy issues. It also helps manage service health and is integrated and automated to use at scale.
- Use cases: Use AWS Health Dashboard to view account-specific health information. You can also use it to plan for lifecycle events or troubleshoot an incident.

## AWS Trusted Advisor
- Helps you align with AWS best practices, prioritize recommendations, and optimize your AWS resources at scale.
- It can be used to optimize cost, efficiency, security, improve performance, and track service limits.

## IAM Access Analyzer
Provides capabilities to set, verify, and refine permissions by analyzing external access and validating that your policies match your corporate security standards.
- Benefits: IAM Access Analyzer provides benefits like refining permissions, validating IAM policies, helping you meet your least privilege goals, and automating IAM policy reviews.
- Use cases: It can be used to set fine-grained permissions, verify who can access what, remediate unused access, and refine and remove broad access.
