### Day08 - Other Compute Services

##### Docker
- A platform that is used to deploy apps.
- Works by packaging apps into containers that can be run on any OS in any machine.
- Apps run the same regardless of the environment.
- Docker images are stored in Docker Repositories.
- In Docker, resources are shared with the host on one server.

##### Elastic Container Service (ECS)
- An AWS service used to launch Docker containers on AWS.
- We must provision and maintain the EC2 instance.

##### Fargate
- Also used to launch Docker containers on AWS.
- But, we do not need to provision the infrastructure (i.e. EC2 instance)
- Serverless offering.
- AWS runs containers for us.

##### Elastic Container Registry (ECR)
- Private Docker Registry on AWS
- This is where we store Docker images so they can be used by ECS or Fargate

##### What is serverless
- A new paradigm where developers don't have to manage servers anymore.
- We just focus on deploying code.
- This doesn't mean that there's no servers running in the background, it's just that we don't manage or provision them.
- Some serverless service so far: Amazon S3, DynamoDB, Fargate, Lambda.

##### Lambda
- This is where we create virtual functions without having to manage servers.
- Intended for short executions.
- They run on-demand with automated scaling.
- Benefits:
  - Pay per request and compute time, with a generous free-tier
  - Integrated with whole AWS services.
  - Event-driven
  - Integrated with many programming languages.
- Lambda pricing is based on calls and duration.

##### Amazon API Gateway
- Useful for building serverless API.
- A fully managed service to create, publish, maintain, monitor, and secure APIs.
- Serverless and scalable.
- Supports RESTful APIs.

##### AWS Batch
- Fully managed batch processing at any scale.
- A "batch" job is a job with a start and an end.
- Batch will launch EC2 instances or Spot Instances and will provision the right amount of computing and memory.
- Runs any runtime as long as it's packaged as a Docker image.
- Relies on EC2 instances (not fully serverless)

##### Amazon Lightsail
- Virtual servers, storage, databases, and networking.
- Ideal for people with little cloud experiences
- Use cases:
  - Simple web applications
  - Development and testing
- High availability but no auto-scaling and limited AWS integrations.

##### Summary
- Docker: container technology to run application
- ECS: runs Docker containers on EC2 instances
- Fargate: run Docker containers without EC2 instances
- ECR: Private Docker Image Repository
- Batch: run batch jobs on AWS across managed EC2 instances.
- Lightsail: lightweight version of AWS
