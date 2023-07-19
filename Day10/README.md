### Day10 - Leveraging the AWS Global Infrastructure

##### Why a Global Application
- Decreased latency and better user experience.
- Disastor Recovery:
  - If an AWS region goes down, we can fail-over to another region and still have our application running.
- Attack protection.

##### Global AWS Infrastructure
- Regions: These are wide geographic zones (i.e. us-east)
- Availability Zones: These are multiple data centers within regions (i.e. us-east-1a, us-east-1b, etc...)
- Edge Locations: These are data centers that deliver content to users fast by utilizing CDN (content delivery network).

##### Route53
- It is a managed DNS (Domain Name System) that routes users to the closest deployment with the least latency
- Recall that a DNS is similar to a phone book in the sense that it translates domain names to IP addresses so that we can access resources from a server.
- Routing Policies:
  - Simple Routing Policy: We make a request to Route53 with a domain name and we get an IP address as a response. No health checks
  - Weighted Routing Policy: This is where Route53 can distribute the traffic into different EC2 instances; effectively it is similar to a load balancer. Health checks are applied.
  - Latency Routing Policy: Depending on where the user is located, they are given access to the closest EC2 instance located geographically. This is to minimize latency.
  - Failover Routing Policy: Route53 will do a health check on the primary EC2 instance and if it's not healthy, it will route the user to a fail-over instance where they can still access the data from the primary EC2 instance. Helps with disaster recovery.

##### AWS CloudFront
- This is a Content Delivery Network (CDN)
- Improves read performance by caching content at the edge locations.
- This improves user experience by minimizing latency.
- There are 216 edge locations currently.
- DDoS protection.
- S3 Cross-Region Replication vs CloudFront
  - CloudFront is a CDN which caches content into points of presence.
  - S3 CRR replicates an entire S3 bucket into a different region for lower latency.

##### S3 Transfer Accelerator
- This is how we transfer files from one S3 bucket in one region to another S3 bucket in another region.
- It accelerates global uploads and downloads into Amazon S3

##### AWS Global Accelerator
- Improves global application availability using the AWS global network.
- Here we leverage the AWS internal network to optimize application performance.
- Global Accelerator vs CloudFront
  - CloudFront is a CDN where content is served from the edge location
  - Global Accelerator: edge locations are a proxy between the request from the user and the application server in other AWS regions. With this, requests are sent through the private AWS internal network.
- Improves global application availability and performance.

##### AWS Outposts
- These are server racks that offer the entire AWS infrastructure to build application on on-prem servers, just as you would in the cloud.
- An extension of AWS services in our own data centers.

##### AWS WaveLength
- Allows for AWS services to be accessible over 5G networks.

##### AWS Local Zones
- These are zones where AWS services are placed closer to the end users to run latency-sensitive applications.
- AWS resources are brought closer to the geographical area of our users.
- Essentially an extension of the Virtual Private Cloud (VPC) into different locations.
- Ideal for latency-sensitive applications.