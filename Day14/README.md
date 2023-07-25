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
- Optimally, we need to encrypt our data in both states.