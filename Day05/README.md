### Day05 - Elastic Load Balancing (ELB) and Auto Scaling Groups (ASG)

##### What does scalability mean?
- Vertical scalability
  - This means to increase the size of the instance itself.
  - For example, upgrading from a t2.micro to a t2.large.
  - This is perfect for non-distributed systems such as databases.

- Horizontal scalability
  - This means to increase the number of instances available.
  - This is ideal for distributed systems, where the functionalities are split across many different instances.

##### High Availability
- This means that your system/application is running in at least 2 availability zones.
- This way you can survive data loss if one instance at a certain availability zone breaks down.

##### Elasticity vs Scalability
- Scalability is the ability of the hardware to be able to handle the workload by either scaling up and down (vertical) or in and out (horizontal)
- Elasticity is the ability to autoscale once the system becomes scalable.

##### What is Load Balancing?
- Load balancers are mechanisms that can direct traffic and workload to many downstream EC2 instances.
- Obviously the benefits from that is that the work is spread across many different EC2 instances. It also means that if an instance is faulty, the load balancer will be able to direct the load away from that instance.
- The Elastic Load Balancer (ELB) provided by AWS automatically does the load balancing. All we have to do is to adjust a few knobs to determine the behavior of the ELB.
- 4 kinds of load balancers:
  1. Application Load Balancer: This handle HTTP/HTTPs traffic (called layer 7 load balancer).
  2. Network Load Balancer: This handles high-performance and TCP/UDP traffic (called layer 4 load balancer)
  3. Gateway Load Balancer: This load balancer directs GENEVE traffic to a virtual security applications to perform firewall applications before it gets to the EC2 instance
  4. Classic Load Balancer (retired in 2023)
- Target groups are a collection of EC2 instances that we can apply load-balancing to. For example, we may have two EC2 instances in our target group. The load balancer targets the group of these instances and will distribute the load amongst these two EC2 instances.

##### Auto Scaling Groups (ASG)
- This is basically a mechanism that add or remove EC2 instances depending on the workload on our applications. It also adds any instances created to a load balancer and replaces any unhealthy instances.
- This optimizes our cost.
- Scaling strategies:
  1. Manual Scaling: update the size of the ASG manually
  2. Dynamic Scaling: 
    - Simple/ Step scaling: update the size of the ASG in response to a cloudwatch alarm.
    - Target Tracking scaling: maintain a certain level of performance (i.e. have the CPU being utilized at 40%).
    - Scheduled scaling: The ASG will add/remove EC2 instances at certain times of the day or at a specific date.
    - Predictive scaling: uses machine learning to predict future traffic. This has the benefit of getting the right amount of EC2 instances in advance.