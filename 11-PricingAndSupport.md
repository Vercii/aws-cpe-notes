## AWS Pricing Concepts
- Pay as you go; you can adapt to changing business needs and reduce the risk of overprovisioning or missing capacity.
- Save when you commit; certain services such as Compute services on AWS, Savings Plans offer savings over On-Demand prices when you commit to a 1-year or 3-year plan.
- Pay less by using more; you can realize important savings as your usage increases. For some services, pricing is tiered, meaning the more you use, the less you pay.

# Main Driving Factors of Cost
## Compute
- For compute resources, you pay by a certain span of time, like by the hour or by the second. Unless you've made a reservation for which the cost is agreed upon beforehand, you pay from the time you launch a resource until the time you stop the instance.

## Storage
- You can choose from a broad portfolio of storage solutions with deep functionality for storing, accessing, protecting, and analyzing data. Pricing for storage largely depends on how much storage you have provisioned or how much you are using.

- For some storage options, such as Amazon Simple Storage Service (Amazon S3), storage cost is tiered. This means you can optimize storage costs based on how frequently and quickly you need to access data. With Amazon S3, consider the following six cost components when storing and managing customer data:
  1. Storage pricing
  2. Request and data retrieval pricing
  3. Data transfer and transfer acceleration pricing
  4. Data management and analytics pricing
  5. Replication pricing
  6. The price to process your data with Amazon S3 Object Lambda

## Data Transfer
- In most cases, there is no charge for inbound data transfer or for data transfer between AWS services within the same Region. There are some exceptions, so be sure to verify data transfer rates before beginning.
-  Outbound data transfer is aggregated across services and then charged at the outbound data transfer rate. The more data you transfer, the less you pay per gigabyte. For data storage and transfer, you typically pay per gigabyte.

# AWS Pricing and Billing Services
## AWS Organizations
- Provides centralized management and governance of your AWS environment. Using AWS Organizations, you can create, group, and manage accounts. You can also apply security policies at the account level and consolidate billing with multiple accounts using a single payment method.
- You can consolidate multiple AWS accounts into one central organization, and implement organization-wide policies.

## AWS Billing and Cost Management Dashboard
- The AWS Billing and Cost Management dashboard centralizes cost management, showing current charges, usage, forecasts, and detailed breakdowns. It also provides tools to manage payments, view invoices, set budgets, and consolidate billing.
- It uses helpful visualizations and billing reports of monthly AWS spend. Sets up and manage payment methods.

## AWS Budgets
- AWS Budgets helps set custom budgets and sends alerts when costs, usage, or Savings Plans and Reserved Instances (RIs) utilization or coverage exceed defined thresholds.

## AWS Cost Explorer
- Helps visualize, analyze, and manage AWS costs and usage with interactive graphs, reports, and forecasts. It provides insights into spending patterns, trends, and Reserved Instance recommendations.

## AWS Pricing Calculator
- A web-based planning tool that you can use to create estimates. You input specific configurations such as instance types, storage options, and data transfer volumes. Then, based on your configurations, you receive a detailed cost breakdown to help you budget for your AWS resource allocation.

# AWS Support Plans
| Basic Support | Developer Support * | Business Support * | Enterprise On-Ramp Support * | Enterprise Support |
| :--- | :--- | :--- | :--- | :--- |
| Included for all AWS customers | Recommended for experimenting or testing in AWS | Recommended minimum tier for production workloads in AWS | Recommended for production and business critical workloads in AWS | Recommended for business critical and mission critical workloads in AWS |
| Includes access to documentation, whitepapers, and AWS re:Post | **Response times:**<br>• < 24 hours for general guidance<br>• < 12 hours when systems impaired | **Response times:**<br>• _Includes previous plan response times_<br>• < 4 hours when production system impaired<br>• < 1 hour when production system is down | **Response times:**<br>• _Includes previous plan response times_<br>• < 30 minutes when business-critical system is down | **Response times:**<br>• _Includes previous plan response times_<br>• < 15 minutes when business- or mission-critical system is down |
| Core AWS Trusted Advisor checks | Core AWS Trusted Advisor checks | Full set of AWS Trusted Advisor checks | Full set of AWS Trusted Advisor checks | Full set of AWS Trusted Advisor checks and prioritized recommendations by AWS account team |
| Technical Account Management not included | Technical Account Management not included | Technical Account Management not included | A pool of technical account managers (TAMs) provide proactive guidance | A designated TAM provides consultative architectural and operational guidance |

