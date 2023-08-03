### Day19 - AWS Architecting

##### General Guiding Principles
1. Stop guessing your capacity needs. Use an auto-scaling group to scale based on the demand on the system.
2. Test system at production scale.
3. Automate to make architectural experimentation easier.
4. Design your architecture in a way to allow it to evolve.
5. Drive architectures using data.
6. Improve through game days; simulate an overloaded system.

##### Design Principles
1. Scalability: vertical and horizontal
2. Disposable Resources: servers should be disposable and easily configured.
3. Automation: serverless, IaaS, auto-scaling, etc...
4. Loose Coupling
  - Build applications that have loosely-coupled components.
5. Think in services, not servers.
  - What managed services we could use.

##### Six Pillars of Well-Architectured Framework
1. Operational Excellence
2. Security
3. Reliability
4. Performance Efficiency
5. Cost Optimization
6. Sustainability

##### Pillar 1: Operational Excellence
- This is the ability of a system to deliver business value and to improve processes.
- Design principles:
  - Perform operations as code - infrastructure as code is a cornerstone of this pillar.
  - Annotate documentation
  - Make frequent, small, reversible changes.
  - Refine operations procedures frequently
  - Anticipate and learn from operational failures.

##### Pillar 2: Security
- This is the ability to protect information, systems, and assets while delivering business value.
- Design principles
  - Implement a strong identity foundation.
  - Enable traceability.
  - Apply security at all layers.
  - Automate security best practices
  - Protect data in transit and at rest
  - Keep people away from data
  - Prepare for security events.

##### Pillar 3: Reliability
- The ability of a system to recover from infrastructure or service disruptions and to dynamically acquire computing resources to meet demand.
- Design principles
  - Test recovery procedures.
  - Automatically recover from failure.
  - Scale horizontally to increase system availability.  
  - Stop guessing capacity.
  - Manage change in automation.

##### Pillar 4: Performance Efficiency
- This is the ability to use computing resources to meet system requirements and to maintain that level of efficiency as demand changes.
- Design principles:
  - Democratize advanced technologies
  - Go global in minutes
  - Use serverless architectures
  - Experiment more often
  - Mechanical sympathy

##### Pillar 5: Cost Optimization
- The ability to run your achitecture at the lowest price point.
- Design principles
  - Pay for what you use.
  - Measure overall efficiency
  - Stop spending money on data center operations.
  - Analyze and attribute expenditure.
  - Used managed and application level service to reduce cost of ownership.

##### Pillar 6: Sustainability 
- Minimize environmental impacts of running cloud workloads.
- Design principles:
  - Understand your impact.
  - Establish sustainability goals
  - Maximize utilization
  - Anticipate and adopt more efficient hardware and software offerings.
  - Use managed services
  - Reduce downstream impact of cloud workloads.

##### AWS Well-Architected Tool
- A free tool to review your architecture against the 6 pillars and adopt architectural best practices.

##### AWS Cloud Adoption Framework (CAF)
- Helps you build a plan for digital transformation through innovative use of AWS.
- Has 6 perspectives:
  1. Business
  2. People
  3. Governance
  4. Platform
  5. Security
  6. Operations

##### Business Capabilities
- Business perspective: helps ensures that cloud investments are congruent with business outcomes.
- People perspective: a bridge between technology and business. Focus on culture, leadership, and organizational structure.
- Governance perspective: orchestrate cloud initiatives while maximizing organizational benefits.

##### Technical Capabilities
- Platform perspective: helps build an enterprise-grade hybrid cloud platform.
- Security perspective: helps achieve integrity of data and cloud workloads.
- Operations perspective: helps ensures that cloud services are delivered at a level that meets business needs.

##### Transformation Domains
1. Technology
  - Using the cloud to migrate and modernize legacy infrastructure
2. Process
  - Automating and optimizing business operations
3. Organization
  - Reimagining operating model
4. Product
  - Reimagining business model by creating new products and services and revenue models.

##### AWS Right Sizing
- This is the process of matching instance types and sizes to your workload performance at the lowest possible cost.
- Start small and always scale up.
- Right Size when:
  - before cloud migration
  - continuously after the cloud onboarding process

##### AWS IQ
- Quickly find professional help for AWS projects.
- Pay 3rd party experts for on-demand project work.

##### AWS re:Post
- AWS-managed Q&A service offering expert-reviewed answers; similar to a forum.

##### AWS Managed Service (AMS)
- A team of people AWS experts that provide infrastructure and application support on AWS.
  - They operate your infrastructure for security, reliability, and availability.
  

