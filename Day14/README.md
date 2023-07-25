### Day14 - Security and Compliance


##### AWS Shared Responsibility Model
- AWS is responsible for security OF the cloud.
- The customer (you) are responsible for security IN the cloud.

##### DDoS (Distributed Denial of Service) Attack
- This is when an attacker launches a large amount of bots to overload our application server. The result of that is that we can't get data from our server since it's overloaded with requests.
- How do we protect ourselves from it:
  - AWS Shield Standard: enabled for all customers at no additional cost
  - AWS Shield Advanced: 24/7 premium DDoS protection
  - AWS WAF: filters requests based on rules.
  - CloudFront and Route53: protection at the edge locations.

##### AWS Shield
- AWS Shield Standard:
  - Free service for every AWS customer.
  - Protects from attacks such as SYN/UDP floods.
- AWS Shield Advanced:
  - Optional and cost $3000 per month per organization.
  - Provides protection against more sophisticated attack on our AWS resources.
  - 24/7 access to AWS DDoS team

##### AWS Web Application Firewall
- Protects web applications from common web exploits.
- Define rules such as IP addresses, HTTP headers, HTTP body, etc...

##### AWS Network Firewall
- Protects your entire Amazon VPC at any direction.

##### Penetration Testing on AWS Cloud
- This is when you attack your own AWS infrastructure to test your security.
- We can conduct these without prior approval for 8 services.
  - Amazon EC2 instances, NAT Gateways, Elastic Load Balancers
  - Amazon RDS
  - Amazon CloudFront
  - Amazon Aurora
  - Amazon API Gateways
  - AWS Lambda
  - Amazon Lightsail
  - Amazon Beanstalk
- Other than that, you would have to contact the AWS security team to approve of penetration testing.

##### Encryption
- Encryption at rest
  - Data stored or archived on a device.
  - Think of data on a hard-disk; it's not moving.
- Encryption in transit
  - Data encrypted while it's being uploaded to an EC2 instance, S3 bucket, etc...
  - Data is encrypted on the network.
- Optimally, we need to encrypt our data in both states. We leverage something using encryption keys.

##### Amazon KMS (Key Management Service).
- This is the go-to encryption for any AWS service.
- Our encryption keys are managed by AWS. But we define who has access to those keys.
- Some services have an opt-in encryption or encryption is enabled by default.

##### Amazon CloudHSM
- Here, AWS gives us the encryption hardware. But we are managing the encryption keys.
- We get a dedicated hardware that is tamper resistant so that it can't be tampered with or accessed by an attacker.

##### AWS Certificate Manager (ACM)
- This allows us to provision, manage, and deploy SSL/TLS certificates which are used to encrypt websites access (i.e. this is how HTTPs works).
- These certs are loaded by ACM onto an application load balancer or APIs, which can give our users HTTPs access to our clients.

##### AWS Secrets Manager
- A service meant to store secrets.
- We can rotate secrets every X amount of days.
- Secrets are encrypted using KMS.

##### Amazon Artifact
- A portal that gives access to AWS compliance documentation and AWS agreements.
- This is how we do internal audits and show compliance in using AWS resources.

##### Amazon GuardDuty
- Intelligent Threat discovery to protect AWS accounts.
- Uses Machine Learning algorithms to detect any anomalies on our account.
- Can be enabled by one click.
- GuardDuty collects logs from different services, create an EventBridge event, which can then send notis using SNS or trigger a lambda function
- Protects against cryptocurrency attacks.

##### Amazon Inspector
- Automated security assessements on:
  - EC2 instances
  - Container images on Amazon ECR images
  - Lambda functions

- It evaluates package vulnerability and network reachability.
- Reports are sent to an AWS Security Hub which then creates an event in EventBridge to see any vulnerabilities on our infrastructure.

##### AWS Config
- Helps with auditing and recording compliance of AWS resources.
- Records compliance, configurations and changes over time.
- We can then set up an SNS notification for any changes.
- This is a region-level service.

##### Amazon Macie
- This is a managed data security and data privacy service that uses machine learning to discover and protect sensitive data in AWS.
- It does that by analyzing sensitive data in our S3 buckets

##### AWS Security Hub
- Central security tool to manage security across several AWS accounts and automates security checks.
- Dashboard that is fully integrated with other AWS accounts to show security and compliance status to allow us to take actions.
- We have to enable AWS Config first.

##### Amazon Detective
- Identifies the root cause of security issues or suspicious activies in our AWS architecture.

##### Root user privileges
- The root user is the account owner.
- Normally, we NEVER want to use the root user account for everyday tasks.
- But there are things that ONLY the root user can that we can't do.
  - Change account settings.
  - View tax invoices.
  - Close AWS account.
  - Change or cancel AWS Support plan.
  - Register as a seller in the Reserved Instance Marketplace.
  - Configure an S3 bucket for MFA
  - Edit or delete an S3 bucket policy
  - Sign up for GovCloud.

##### IAM Access Analyzer
- Finds our which resources are shared externally.
- It's done by defining a Zone of Trust, which is a collection of entities that can access our resources.

##### Summary
- Shared Responsibility 
- Shield: Automatic DDoS protection
- WAF: firewall to filter requests based on rules
- KMS: encryption keys managed by AWS
- CloudHSM: hardware encryption, but we manage keys.
- ACM: provision, manage, and deploy SSL/TLS certificates
- Artifact: access to compliance reports
- GuardDuty: find malicious behavior with VPC and CloudTrail Logs
- Inspector: assess secutiy and finds software vulnerabilities in AWS resources. It is automated.
- Network Firewall: protects your VPC against network attacks
- Config: track config changes and compliance
- Macie: finds sensitive data in Amazon S3 buckets
- CloudTrail: tracks API made by users within an AWS accound
- AWS Security Hub: gather security data from multiple accounts
- Amazon Detective: find the root cause of security issues or suspicious activities
- AWS Abuse: reports AWS resources for abusive or illegal purposes.
- Root user privileges
- IAM Access Analyzer: identifies which resources are shared externally.