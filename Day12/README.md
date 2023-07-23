### Day12 - Cloud Monitoring

##### Amazon CloudWatch Metrics
- Service that provides metrics for services in AWS.
- Metrics include CPU utilizations, network performance, etc...

##### Amazon CloudWatch Alarms
- These are notifications that are triggered if one or more metric reach a certain threshold.

##### Amazon CloudWatch Logs
- This is a service that collects logs from various AWS services.
- Logs are basically text that indicates how the app is doing.
- CloudWatch logs allows for real-time monitoring of logs.
- By default EC2 instances do not send logs to CloudWatch Logs. We have to install a CloudWatch agent on an EC2 instance to push log files.
- This same agent can also be installed on on-prem servers.

##### Amazon EventBridge (formerly known as CloudWatch Events)
- This is a way to manage integrations between different applications and services within AWS.
- For example, you can use EventBridge to schedule Cron jobs, which are scripts of code that run on a certain schedule.
- Or you could use it to trigger a certain event if a user does something within the AWS console.
- We can also EventBridge to handle events from AWS partners such as ZenDesk and DataDog as well as create our own custom event handling bus.

##### Amazon CloudTrail
- Provides governance, compliance, and audit for your AWS account.
- You get a history of events/API calls within your AWS account.
- You can send this to CloudWatch Logs or an S3 bucket in order to retain the logs provided by the CloudTrail Console.

##### AWS X-Ray
- This is a way to get a visual analysis of our applications.
- Ideal for troubleshooting performance, identifying issues with different services, finding errors and exceptions, and so on.
- This is a way to visualize distributed services (i.e. microservices architecture).

##### Amazon CodeGuru
- a ML service for automated code reviews(CodeGuru Reviewer) and provides recommendations for application performance (CodeGuru Profiler).
- CG Reviewer can identify critical issues, security issues, and other bugs.
- CG Profiler identifies runtime behavior of our applications.

##### AWS Health Dashboard
- Service History:
  - Shows all the services across all the different regions.
- Your Account:
  - Provides alerts when AWS is experiencing events that may impact you.

##### Summary
- CloudWatch:
  - Metrics: monitor the performance of AWS services
  - Alarms: send notifications based on metric performance and automate certain actions.
  - Logs: collects log files from various AWS service.
  - Events: react to event in AWS
- CloudTrail: audit API calls made within your AWS account
- CloudTrail Insights: analysis of CloudTrail Events.
- X-Ray: trace requests within a distributed system
- Health Dashboard: status of all AWS services across all regions
- Account Health Dashboard: status of AWS services that impact our infrastructure.
- CodeGuru: automated code reviews + application performance recommendations.