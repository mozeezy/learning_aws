### Day09 - Deploying and Managing Infrastructure at Scale

##### CloudFormation
- A declarative way of outlining AWS infrastructure and services by leveraging infrastructure as a service. All we have to do is just write the code and AWS will handle setting up the infrastructure. This is known as Infrastructure as a Code (IaC)
- Allows us to use repeated architecture for different environments and regions.

##### AWS Cloud Development Kit (CDK)
- Allows us to define cloud infrastructure using a programming language
- The code is then compiled into a cloudformation template, which would create the architecture.

##### AWS Beanstalk
- A service that allows developers to deploy applications on AWS.
- An example of PaaS because it allows developers to focus on code only, while AWS handles the creation of EC2 instances, load balancers, and all the necessary infrastructure to make sure that our app can scale automatically.
- It is a managed service and we pay for the underlying instances.
- It also has health monitoring capabilities which checks for app health and pushes metrics to CloudWatch.

##### AWS CodeDeploy
- It is a way to deploy applications academically with each upgrade.
- Works with EC2 Instances and On-Premises servers.
- But we have to provision the servers and instances ahead of time with the CodeDeploy Agent, which will handle setting up the infrastructure to upgrade our application.

##### AWS CodeCommit
- Similar to GitHub, but is an AWS service.
- Fully managed; scalable and highly available.

##### AWS CodeBuild
- Allows us to build our code in the cloud.
- Compiles source code, run tests, and produces a ready-to-deploy prototype.
- Fully managed and serverless.
- Continuosly scalable and highly available and secure.
- Pay-as-you-go pricing.
- A typical architecuture:
  CodeCommit <---Retrieve code--- CodeBuild ---Build code--> Ready-to-deploy

##### AWS CodePipeline
- Allows us to define steps so that the code can automatically pushed to production.
- This is the basis of CICD
- Fully managed service
- Fast delivery and rapid updates.

##### AWS CodeArtifact
- A service that manages, stores, and retrieves software packages (i.e. dependencies for our application). 
- Works well with other dependency management tools such as npm.

##### AWS CodeStar
- A UI that manages software development and setting up the infrastructure (i.e. CodeCommit, CodeArtifact, etc...).

##### AWS Cloud9
- This is a cloud IDE that allows us to write, run, and debug code. This is an IDE on the browser.
- Allows for pair-programming.

##### AWS Systems Manager (SSM)
- Helps manage EC2 and On-Premises systems at scale (i.e. hybrid service).
- Conducts patch automation on EC2 instances and on-prem systems for enhanced compliance.
- SSM Session Manager:
  - allows to start a secure shell on EC2 and on-prem servers with SSH keys.

##### AWS OpsWork
- An alternative to SSM that allows for automatic server configurations and repetitive commands.
- It is a managed service that is similar to Chef and Puppet.

##### Summary
- CloudFormation: Infrastructure as Code (IaC) -> a service that sets up the underlying infrastructure using code (i.e. JSON/YAML). It is compatible with almost all of AWS resources.
- Beanstalk: Platform as a service (PaaS) -> Here we have an infrastructure already set up and can scale automatically. All we have to do is write our application code and Beanstalk will set up the necessary infrastructure to run the application.
- CodeDeploy: deploy application on servers following an automated process.
- Systems Manager: patch, configure, and run commands across EC2 instances and on-prem infrastructure.
- OpsWorks: similar to Chef and Puppet.

- CodeCommit: store code in a private git repo.
- CodeBuild: builds and test code in AWS.
- CodeDeploy: deploy code onto servers
- CodePipeline: creates a pipeline following CI/CD.
- CodeArtifact: stores software packages and dependencies on AWS.
- CodeStar: a UI that allows developers to create projects without having to set up pipelines, repos, etc..
- Cloud9: a cloud IDE
- CloudCDK: defines the cloud architecture using a programming language.
