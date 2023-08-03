### Day18 - Account Management, Billing & Support

##### AWS Organizations
- Global service that allows you to manage multiple AWS accounts.
- Main account is called the master account.
- Consolidated billing.
- You can Service Control Policies (SCP) to restrict account privileges.
- Multi-Account strategies can be used to create multiple accounts per department, per team, on different VPCs with different SCPs.
  - Enable CloudTrail on all accounts to send logs to central S3 account.

##### Organizational Units (OU)
1. Business unit
2. Environmental Lifecycle
3. Project-based

##### Service Control Policies (SCP)
- Whitelist or blacklist IAM actions.
- Applied at the OU or Account level.
- Doesn't apply to Master account.
- SCP must have explicit allow. 

##### Consolidated Billing
- One Bill for all AWS Accounts in the AWS Organization.
- Combined usage of all AWS accounts within your organization to share volume pricing, Reserved Instances, and Savings Plans discounts.

##### AWS Control Tower
- Easy way to set up and govern a secure and compliant multi-account AWS environment based on best practices.

##### AWS Resource Access Manager (RAM)
- Allows you to share AWS resources with other AWS accounts.
- Some resources include Aurora, VPC subnets, EC2, etc...

##### AWS Service Catalog
- This is a self-service portal that allows AWS users to launch a set of authorized products pre-defined by admins.

##### Pricing Models in AWS
1. Pay-as-you-go: pay for what you use.
2. Save when you reserve: comply with long-term requirements.
3. Pay less by using more: volume-based discounts.
4. Pay less as AWS grows

- There are free services and free-tier services in AWS.

##### Savings Plan
- It is a commitment to spend a certain dollar amount per hour for 1 or 3 years.
- EC2 Savings Plan
- Compute Savings Plan
- Machine Learning Savings Plan

##### AWS Compute Optimizer
- Used to reduce costs and improve performance by recommedning optimal AWS resources for the workload.
- Utilizes Machine Learning to analyzing resources' configurations.

##### Billing and Costing Tools
- Estimating costs in the cloud
  - Pricing calculator
- Tracking costs in the cloud
  - Billing dashboard
  - Cost allocation tags
  - Cost and usage reports
  - Cost explorer
- Monitoring against cost plans
  - Billing alarms
  - Budgets.

##### AWS Pricing Calculator
- This gives an estimate of the cost of your solution architecture.

##### AWS Billing Dashboard
- This is a UI that shows you the cost of the underlying services of your AWS architecture.
- Use cost allocation tags to track AWS costs on a detailed level. It provides a way to organize resources. 

##### Cost and Usage Reports
- A detailed report about your AWS costs and usage.

##### Cost Explorer
- A visual way to understand and manage AWS costs and usage over time.
- Allows you to forecast usage up to 12 months based on previous usage.

##### Billing Alarms in CloudWatch
- Billing data metric is stored in CloudWatch us-east-1
- This metric is for the actual cost of overall AWS services.

##### AWS Budgets
- You can send alarms when cost of AWS services exceed the budget set by us.

##### AWS Cost Anomaly Detection
- Uses ML to detect unusual spends for cost and usage of AWS services.
- Sends you a report with the root-cause analysis.

##### AWS Service Quotas
- Notifies you when you're close to reaching a service quota value threshold.

##### AWS Trusted Advisor
- Assess your AWS account.
- Provides recommendation on 5 categories:
  - Cost optimization
  - Performance
  - Security
  - Fault tolerance
  - Service limits

- Support plans
  - Basic and Developer Support Plan
    - S3 bucket permissions
    - Security Groups
    - IAM Use
    - MFA on Root Account
    - EBC Public Snapshots
    - RDS Public Snapshots
    - Service Limits
  - Business and Enterprise Support plan
    - Full checks on the 5 previous categories
    - Ability to set CloudWatch alarms when reaching limits.
    - Programmatic Access using the AWS Support API

##### AWS Support Plans Pricing
- Basic
  - Customer Service and communities
  - Access to the 7 Trusted Advisor checks
  - Access to AWS Personal Health Dashboard

- Developer
  - All Basic Support plan
  - Business hours email access to Cloud Support Associates
  - Unlimited cases

- Business
  - Intended for production workloads
  - Full set of checks by Trusted Advisor
  - 24/7 phone, email, and chat access to Cloud Support Engineers.
  - Unlimited cases and unlimited contacts

- Enterprise On-Ramp
  - Intended if you have production or business-critical workloads
  - Access to a pool of Technical Account Managers
  - Concierge Support Team

- Enterprise
  - Intended to be used if you have mission-critical workloads
  - Access to a designated Technical Account Manager
  - Concierge Support Team


##### Account Best Practices
- AWS Organizations: operate multiple accounts
- Service control policies (SCP): restricts account power.
- AWS Control Tower: an easy way to setup multiple accounts with best practices.
- Tags and Cost allocation tags: easy account and billing management.
- IAM guidelines: enabling MFA, least-privilege, creating password policy, and enabling password rotation
- Config: records all resource configurations and compliance over time.
- CloudFormation: deploy stacks across accounts and regions
- Trusted Advisor: get insights and support plan according to needs.
- Send service and access logs to S3 or CloudWatch logs.
- CloudTrail: track API calls made within your account.
- AWS Service Catalog: allow users to create pre-defined stacks defined by admins.

##### Billing Summary
- Compute Optimizer: recommends resources to reduce cost.
- Pricing Calculator: estimated cost of services
- Billing Dashboard: a visual of usage of services.
- Cost Allocation Tags: tag resources to create reports.
- Cost and Usage Reports: mosst comprehensive billing dataset. 
- Cost Explorer: view current usage and forecas usage
- Billing Alarms: only available in us-east-1 and tracks per-service billing
- Budgets: tracks usage of services based on budget set by user.
- Savings Plans: save more through long-term usage of AWS.
- Cost Anomaly Detection: detect unusual spends.
- Service Quotas: notify when approaching a service quota threshold.