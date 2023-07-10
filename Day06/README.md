### Day06 - Amazon S3

##### What is S3

- It is an AWS service that is used for storage and backup; disastor recovery; archiving; application hosting; and media hosting.
- Amazon S3 stores objects (i.e. files) in "buckets" and must have a globally unique level.
- S3 buckets are defined at the region level
- Objects in S3 have a key and that key is the full path from the top-level directory.
  - i.e. (my-s3-bucket/my_file.txt) -> "my_file.txt" is the key.

##### S3 Security

- User-based:

  - IAM policies: from the IAM dashboard, we can control which user can access the S3 bucket.

- Resource-based:
  - Bucket policies: these are policies that can set across the entire bucket from the S3 dashboard. This also allows for cross-account access.

##### S3 Bucket Policies

- Just like the IAM policies, these are JSON-based policies.
- It contains details about which resources we can access within the bucket (i.e. objects and files); the effect (i.e. allow or deny access); actions (i.e. what resources do we have access to); and the principal (i.e. who does this policy apply to).
- These bucket policies can be used to give public access to our bucket.
- We can create an S3 bucket policy using the policy generator from the S3 console.

##### S3 and Website hosting

- We can use S3 to host our websites. However, since the website uses a public IP address, we must attach a bucket policy to give the public access to our S3 buckets.

##### S3 Versioning

- We can also version files in S3.
- This allows us to access the version history of our files and rollback to a previous version, if errors were to occur.

##### Replication

- To allow for bucket replication, we must enable versioning in the source and destination buckets as well as set up the correct IAM permissions.
- Replication is an asynchronous process, which means that it happens in the background.
- Cross-Region Replication (CRR)
- Same-Region Replication (SRR)

##### S3 Storage Classes

1. Amazon S3 Standard - General Purpose
2. Amazon S3 Standard - Infrequent Access (IA)
3. Amazon S3 One Zone-Infrequent Access
4. Amazon S3 Glacier Instant Retrieval
5. Amazon S3 Glacier Flexible Retrieval
6. Amazon S3 Glacier Deep Archive
7. Amazon S3 Intelligent Tiering

- We can move between classes manually or through the S3 Lifecycle configuration.

##### S3 Durability and Availability

- Durability: this is a metric that measures how often an object is going to be lost by S3.
  - S3 is highly durable (11 9s i.e. 99.999999999%).
  - This is the same for all storage classes
- Availability: this is how readily available a service is.
  - varies according to the storage class.

###### Storage Classes Comparison Table

| S3 General Purpose                                                       | S3 Infrequent Access                        | One Zone Infrequent Access                                   | Glacier Instant Retrieval                                                            | Glacier Flexible Retrieval                                                               | Glacier Deep Archive                                  | Intelligent Tiering                                             |
| ------------------------------------------------------------------------ | ------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------- | ----------------------------------------------------- | --------------------------------------------------------------- |
| 99.99% availability                                                      | 99.90% availability                         | 99.5% availability                                           | Mostly for archiving/backups                                                         | Has three flexibilites: expedited (1-5 mins), standard (3-5 hours), and bulk(5-12 hours) | Has two tiers: standard (12 hours) and bulk(48 hours) | Moves objects between the different access tiers based on usage |
| Low latency and high throughput                                          | These are for less frequently accessed data | Storing data in a single AZ; data is lost if AZ is destroyed | Allows for milliseconds data retrieval and has a minimum storage duration of 90 days | Minimum storage of 90 days                                                               | Minimum storage duration of 180 days                  | There is a small monitoring fee + auto-tiering fee.             |
| Ideal for content distribution, big data, gaming applications, and more. | Ideal for data recovery and backups         | Ideal for storing secondary backups and replicated data      | For all glacier storage classes, you pay for the storage and retrieval.              |                                                                                          | Ideal for long-term storage                           | No cost on retrieval                                            |


