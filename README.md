# AWS Cloud Practitioner

## Documentation
---
## S2E1 - Intro to AWS
[Q&A - Jon](https://www.twitch.tv/aws/video/770438975)
and
[Episode - Jon](https://www.twitch.tv/aws/video/770429171)

- [AWS Global Infrastructure](https://infrastructure.aws/)
- [Six Advantages of Cloud Computing](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)
- [Overview of Object Storage](https://aws.amazon.com/what-is-cloud-object-storage/)
- [Amazon Simple Storage Service (Amazon S3) Documentation](https://docs.aws.amazon.com/s3/index.html)


**cloud computing** = on-demand delivery of IT resources via the Internet with a pay-as-you-go pricing <br/>
*IT resources*: compute, storage, db <br/>
on-demand + resources + via the Internet = APPLICATIONS

### Deployment models (for applications)
- *on-premises* - everything is on site
- *on cloud* - everything is on cloud
- *hybrid* - some parts can be on premise and some in cloud (e.g., the frontend might be in cloud but the backend and the db on premise)

### 6 benefits of Cloud Computing
- trade capital expenses to bariable expenses
    - don't invest on infrastructure & pay only for what you consume
- economies of scale
    - you can achieve a lower variable cost that you can on your own
    - AWS gives you lower pay-as-you-go prices
    - you can test better infrastructures without buying them
- stop guessing for capacity
    - get when you need more
- increase speed & agility
    - reduce the time to make the resources available => *AGILITY*
- stop spending money on running & maintaining data centers
    - focus on the projects and not on the infrastructure
- go global in minutes
    - 24 regions - minimum 2 Availability Zones each
    - one AZ has one or more Data Centers
    - the atency between 2 AZs (in a Region) should be <10ms ("single digit millisecond latency") - usually it is 1ms
    - Point of Presence / Edge Location (for this certification they are the same)
    - PoP = includes Edge Locations + Regional Edge Cache Servers
    - PoP - cache data closer to the user (220 across the world)
    - there are 6 services available within a PoP / Edge Location

### How to interact with AWS
- AWS Management Console
- CLI
- SDK

### S3 - Amazon Simple Storage Service
- object service storage
- offers scalability, data availability, security, performance

*object storage* = computer data storage architecture that manages data as objects
*file system storage* = computer data storage architecture that manages data as file systems
*block storage* = computer data storage architecture that manages data as blocks within sectors and tracks

*Block storage* is more efficient for changes & for frequently changing data but it is harder to manage. That's why block costs more than storage (because of the overhead for management). <br/>
*Object storage* is more often used for writing the data once & reading it back many times.

S3 is used for media hosting - the hosting account that stores & delivers your audio, video, documents, etc <br/>
S3 can be used to upload backup files, or store & host websites

The objects are in **buckets**:
- there is no limit on the amount of the storage
- file limit is 5TB
- the buckets are globally unique

Other features:
- versioning 
    - when deleting a file / an obejct a *delete marker* is added; you can delete the delete marker
    - \> Properties > Versioning
- lifecycle policies
- object locking
- encryption
    - server side encryption, *encrypted data at rest*
    - \> Properties > Encryption
    - *encryption on transit* - S3 buckets are available over HTTPS to leverage SSL, TLS
- for hosting a website, the bucket needs to be made public
    - by default, an S3 is private
    
    - \> Permissions > Block public access check
    + at the account level (left menu) > "Account Settings for Block Public Access"
    + go to the files and make them public

**S3 Glacier**
- used for long-term data archiving

For the different types of S3s important characteristics are:
- number of Az
- availability
- how you retrieve data
- durability

### S3 vs EBS
S3:
- object storage
- 5 TB max Object size
- unlimited capacity
- low storage cost, you pay for what you use
- avilable over HTTPS

EBS:
- block storage
- gets attached to EC2 instances as hard drives
- provisioned capacity where you pay for what you provisioned

---
## Resources
- [Documentation for the Twitch series](https://pages.awscloud.com/awspowerhour_cloud_practitioner_resources.html)
- [AWS Power Hour (Twitch Series)](https://www.twitch.tv/search?term=aws%20power%20hour%20cloud%20practitioner%20&type=videos)
- [AWS Training](https://www.aws.training/)
- [AWS Cloud Practitioner Essentials](https://www.aws.training/Details/eLearning?id=60697)
