### Day04: EC2 Instance Storage

#### Elastic Block Storage (EBS)
- This is a storage volume that could mounted on an EC2 instance. This is the same way you would plug in a USB drive to your computer.
- These can store various types of files such as databases and file systems and many other applications.
- Allow for data to persist independent from a specific EC2 instance.

#### EBS Snapshots
- Snapshots are backup data that is created by copying an EBS volume at a certain point in time.
- This is a good way to prevent permenant data loss as you can restore the instance to the snapshot, which would restore the EC2 instance to a previous state where the data was not lost.

#### Amazon Machine Images (AMI)
- This is an image file where instances can be launched from.
- These image files contain operating systems, networks, application servers, and other applications that are necessary to create EC2 instances.
- There's an added benefit of faster EC2 instance boot-up time.
- Analogy: gaming disks contain image files which include various different files and configurations that is necessary for the game to work. This makes it easier to play games since the only thing you have to do is just insert the disk and play; we don't have to worry about installing the image file everytime we play the game.

#### EC2 Image Builder
- This is an AWS service that makes it easier to create, manage, and test image files.
- These are image files that we own and can share on the AWS marketplace.
- We have the responsibility to maintain those image files and update them when necessary.

#### EC2 Instance Store
- These are temporary storage volumes for EC2 instances.
- They can deliver high I/O performance.
- If an instance is terminated, all data on an EC2 instance store is lost.
- But, if an instance reboots, then data persists.

#### Amazon Elastic File System (EFS)
- This is a service that is responsible for managing Network File Systems (NFS) in the cloud.
- It can be mounted to various EC2 instances in different AZs, simulataneously (i.e. highly scalable).

