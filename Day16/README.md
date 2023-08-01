### Day16 - Advanced Identity

##### AWS Security Token Service (STS)
- This service enables us to create temporary credentials to use AWS services.
- These are short-term credentials.

##### Amazon Cognitio
- This is a way to provide identiy for users of your web and mobile applications.
- Instead of creating an IAM user, you would create the user in Cognito.
  - IAM user is only for people working in your company and need access to AWS services.

##### AWS IAM Identity Center
- This is a one-login account for all AWS accounts within your organization

##### Summary
- IAM: identity and access management inside AWS account.
- Organizations: a way to manage multiple accounts
- STS: temporary short-term credentials to access AWS resources
- Cognito: create a database of users for web and mobile applications
- Directory Services: integration of Microsoft Active Directory in AWS.
- IAM Identity Center: one login for multiple AWS accounts.