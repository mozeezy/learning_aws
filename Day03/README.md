### Day03 - Elastic Computing Cloud (EC2)

#### What is EC2?
- Essentially, it is a virtual server machine that you "rent" from the cloud provider (i.e. AWS).
- In the world of AWS, these servers are known as instances.
- AWS allows us to use as many of these instances as possible for all possible computing and IT operations, provided that you pay for what you use.
- This gives of the advantage of easily scaling up and down without the need to purchase extra hardware, operating systems, security, and other fees associated with owning an on-premise machine.

#### How to create an EC2 Instance

##### Step 1 - Choose an Amazon Machine Image (AMI)
- This is a file that contains information about the operating system and other software that is used to create EC2 instances.

##### Step 2 - Choose an Instance Type
- An instance type is the hardware that is associated with computing, memory, and storage for the EC2 instance being created.
- i.e. CPUs, Memory, RAM, etc...
- Many types:
  - General Purpose: Balance levels of computing, memory, and storage
  - Compute-Optimized: Instances with high levels of computing powers. Ideal for tasks that require high levels of performance
  - Memory-Optimized: Instances that are ideal for working with huge datasets to be processed in memory.
  - Accelerated Computing: Instances that use co-processing to handle heavy-processing tasks such as graphics processing
  - Storage-Optimized: Instances that are ideal for quick read and write operations on huge datasets.

##### Step 3 - Configure Instance Details
- Here is where you select how many instances you need, purchasing options, network, creating public IP addresses.
- What are the different instance purchasing options?
  1. On-demand instances:
    - This is the default payment method; You pay for what you use.
    - You can start, stop, and terminate instances as much as you like.
    - Ideal for short-term workload.
  2. Reserved instances (RIs):
    - Provide discounted rates (up to 72% compared to on-demand).
    - But, you have to commit to either a 1-year term or a 3-year term.
    - You can pay an entire upfront amount, partial upfront, or no upfront payment at all.
    - Ideal for steady and predictable workload.
    - Three types of RIs:
      - Standard RIs: You can't change your instance type.
      - Convertible RIs: You can change your instance type, but there's a much lower discount (~ 54%). However, the new convertible reserved instance must have a higher value than the original instance.
      - Scheduled RIs: scheduled lauching and termination of instances.
  3. Spot Instances:
    - Provide even steeper discounted rates (up to 90%).
    - Basically, it allows you to request unused instances provided by AWS.
    - However, these instances are not always available and can be easily cancelled with little to no notice.
    - This can be an ideal solution if you don't want a hefty bill, and the nature of the workload can be interrupted.
  4. Dedicated Host: 
    - You pay for a fully dedicated physical server to run your instances, but you have control of the hardware.
    - Analogy: You pay for an entire building.
  5. Dedicated Instances:
    - Like dedicated host, you get a physical server. However, you pay only for the instances that run on that server.
    - Analogy: You only pay for certain rooms in a building.

##### Step 4 - Add Storage
- Here is where you can add Elastic Block Stores (EBS) -- which are volumes -- to your instances. Think of a C: drive in windows, which allows for persistence of data.

##### Step 5 - Configure Security Groups
- These are firewall rules that controls who can access the EC2 instance.

##### Step 6 - Review and Obtain Key Pair
- A key-pair is what allows to connect to the instance. They're credentials -- like a username and a password.