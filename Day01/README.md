## Day01 - What is Cloud Computing

#### Definition
- Cloud computing is the ability to access various IT services on demand on a pay-as-you-go basis.
- What are these IT services?
  - Things like creating servers, storing and analyzing data, creating and managing networks, and much more.

#### Scenario
- Imaging you're developing a web application on your machine and you're excited to share it with the world so you chose to create a public IP address associated with your application.
- Obviously, this means that you must leave the server (i.e. your machine) running to be able to handle the incoming traffic from users on your website.
- But what if the traffic is too much for your machine to handle?
- Maybe you decided to build a physical server (i.e. a large computer with huge computing powers) to handle traffic and user data.
- Now, what if your application had even more users than your first server can handle? 
- You think that it's time to buy another one. 
- So now you have two server machines.
- What if traffic dies down? Now you have an extra server machine that is not even being used.

#### Analysis of the scenario
- From the scenario above, this was how companies used to handle their IT operations; by having machines and servers that would handle IT operations ON-PREMISE.
- This can have several challenges.
  - The need for a large physical space to hold these computers (i.e. data centers).
  - The need to have a dedicated team for maintenance.
  - It makes it hard for a company to scale up or down.

#### Enter the Cloud
- The cloud is essentially a virtual data center that has many servers used for different IT purposes.
- These servers provide various on-demand services and are maintained by cloud providers (i.e. AWS). This eliminates the need for companies to invest huge amounts of capital and expertise into building and maintaining physical servers.
- A huge benefit of the cloud is that it allows for companies to scale up or down as they please, since cloud services follow the pay-as-you-go model.
  - This means that you only pay for what you need and use.

#### Cloud Delivery Models
1. Infrastructure as a service (IaaS)
  - In this model, the cloud providers only provide the data center while allowing users the flexibility of having their own operating systems, application, and security.
  - Analogy: You're given a house (i.e. infrastructure) by the landlord, but you're free to buy the furniture and decorate however you want as long as you're paying the landlord their rent.

2. Platform as a service (PaaS)
  - In this model, the cloud providers provide the data center as well as the operating systems and allows the user to focus on application development.
  - Analogy: You're given the house plus a bit of furniture by the landlord. All you have you to worry about is getting other pieces of furniture, but you still continue to pay rent to the landlord.

3. Software as a service (SaaS)
  - In this model, the cloud providers provide everything. The only thing users are responsible for is who can access these applications and managing the underlying software.
  - Analogy: You're given the house fully furnished. All you have to do is just move in and pay the montly rent.

#### Cloud Deployment Models - How these services actually get to you.
  1. Public Cloud
    - Services are delivered through a public cloud that anyone could use and is managed by the cloud services provider (i.e. multitenancy).
    - Imagine having a common room in a building that is shared by the different tenets in the building.
  
  2. Private Cloud
    - Services are delivered through a private cloud and are that is managed exclusively by you.
    - Think of taking your own car to work instead of taking the public transit.

  3. Hybrid Cloud
    - A mix of both the public and private cloud.
    - Think of renting a car to go on a trip.

#### Shared Responsibility Model
  - This is an infrastructure that details how the relationship between the cloud providers and the users should be.
  - Basically, the cloud is responsible for maintaining the infrastructure and their security of their services while the user is responsible for how to use said infrastructure.
  - Analogy: This is like a lease agreement when you either buy a house or a car. The landlord or the rental company is responsible for making sure that the house or the car is in a good condition, while you're responsible for how to use those things.