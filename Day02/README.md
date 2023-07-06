### Day 02 - Idenity and Access Management (IAM)

#### What is IAM
- IAM is a service that controls who can access AWS services (i.e. authentication) and what can they do with them (authorization).
- When you first create an AWS account, the initial entity that can access all the services on AWS is called the root user.
- A good practice is to never use the root users unless the action can only be performed the root user.
- Rather, it is best to create different IAM users and assign them permissions to use some of the services.

#### Components of IAM
1. Users
  - These are entities (either individuals or applications) that can use the different services, if they have permission to use it.
  - By default, new users do not have authorization to perform any actions with AWS.
  - The root user would have to assign permissions to different users.
  - For example, user-1 may have the dynamodbreadonly permission attached to them and user-2 may have the dynamodbreadandwrite permission attached to them. These users can interact with dynamoDb service under those permissions only.

2. Groups
  - A collection of IAM users that also have access to AWS services with certain permissions.
  - For example, we can create an admin group and an intern group where users in the admin group have the adminstatoraccess permission and the intern group has the readonly permission attached.
  - Users in each group can only interact with AWS services under those permissions only.
  - Users can belong to multiple groups.

3. Policies
  - Documents that detail who can use the different services and what they can do with it.
  - Analogy: Think of a contract that gives you an authorization to do certain things within your company.
  - Two types of policies: 
    1. Managed Policy: this is a policy that is attached to multiple entities (i.e. IAM users and groups)
    2. Inline Policy: this is a policy that is attached to a single entity.

4. Roles
  - These are entities that can access AWS services on behalf of anyone that uses them. They are like IAM users in the sense that they have permissions attached to them. But they are different in the sense that they're not associated with a single entity, but is used by anyone who needs it.
  - They also have an added benefit of not having credentials like passwords or access keys. Rather, they have temporary credentials that are valid for the length that they're used for.
  - Analogy: Think of punch cards/key fobs to access a building. Only those with punch cards can enter the building while the rest are denied access.