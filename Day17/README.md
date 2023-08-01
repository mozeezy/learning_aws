### Day17 - Other AWS Services

##### Amazon WorkSpaces
- Managed Desktop as a Services (DaaS) to provision Windows or Linux desktops.
- Think of virtual desktops.

##### Amazon AppStream 2.0
- Desktop application streaming service.
- You do not need to provision the underlying infrastructure.
- The application can be accessed within the web browser.

##### AWS IoT Core
- Allows you to connect IoT (internet of things) devices to the AWS Cloud.
- Serverless, secure, and scalable.
- Integrates with a lot of AWS services.

##### Amazon Elastic Transcoder
- Allows you to convert media files in S3 into media files formatted by consumer playback devices.
- Fully managed and secure.

##### AWS AppSync
- It is a backend for mobile and web applications.
- Leverages GraphQL.
- Integrates with DynamoDB and Lambda.

##### AWS Amplify
- A set of tools and services that helps with developing and deploying scalable full stack web and mobile applications.

##### AWS Device Farm
- Fully managed service that tests your web and mobile apps against desktop browsers, mobile devices, and tablets.

##### AWS Backup
- Fully managed service to manage and automate backups across AWS services.
- Cross-region backups and cross-account backups.

##### Disaster Recovery
- Backup and Restore
  - Data is stored somewhere in the cloud and in case of a disaster, it can be used to restore the data.
  - Cheap and very minimal cost.

- Pilot Light
  - We have the core functions of the app, but very minimal setup.
  - We don't have an application server.

- Warm Standby
  - Full version of the app is available in the cloud but at minimum size.

- Multi-Site/Hot-Site
  - We have the full version of the app at full size.
  - Most expensive option

##### AWS Elastic Disaster Recovery (DRS)
- Allows you to quickly and easily recover physical, virtual, and cloud-based servers into AWS.

##### AWS DataSync
- Allows you to move large amount of data from on-premises to AWS.
- Data can go into Amazon S3 buckets or EFS.
- Replication tasks can be scheduled hourly, daily, weekly and are incremental.

##### AWS Application Discovery Service
- Plan migration projects by gathering information about on-premises data centers.

##### AWS Application Migration Service
- Allows you to rehost solutions which would simplify migrating applications to AWS.
- Converts your physical, virtual, and cloud-based servers to run natively on AWS.

##### AWS Migration Evaluator
- Helps you build a data-driven business case for migration to AWS.
- Provides a clear baseline of what your organization is running today and develop a migration plan.

##### AWS Fault Injection Simulator (FIS)
- A fully managed service for running fault injections on AWS workloads.
- Leverages Chaos Engineering principles by stressing an application to see how the system would respond. 

##### AWS Step Functions
- It is a serverless visual workflow to orchestrate Lambda functions.
- Integrates with a lot of different AWS services.

##### AWS Ground Station
- Fully managed service that lets you control satellite communications, process data, and scale satellite operations.
- You can dowload satellite data to your AWS VPC or an S3 instance.

##### AWS Pinpoint
- It is an inbound/outbound marketing communications service.
- Supports email, SMS, push and voice messaging.
- It is a 2-way communication system: you can receive replies.
- Ideal for marketing campaigns.