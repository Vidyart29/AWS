What i believe in is -
There is only one success - to be able to spend your life in your own way.

### Services cover in AWS Developer cert
![alt text](image-22.png)

##### 1.  What is AWS?
![Summary](image-1.png)

#### 2. AWS Global Infrastructure:
Regions:
- Regions of aws are all around the world.
- name can be us-east-1(US east) ap-south-1 (mumbai)
- Its a cluster of data center.



#### 3. Selecting a region:
![alt text](image-3.png)

- **Compliance** with data governance and legal requirements: data never leaves a region without your explicit permission.
- **proximity** to customer:  you should select a region as close to your customer as possible to provide low latency.
- for eg: if customers are from SA and resources are in indian region than the equest has to travel all accross the global leading to high latency and low quality of user experience.
- **services available**: not all new services are available in every region. 
  - plan on which services would be required and good fit for your bussiness.
- pricing: vari
#### 4. AZ:
- Availabilty zones are what goes inside the region.
![alt text](image-4.png)

Edge Locations vs Local Zones
![alt text](image-5.png)

Acessing Aws:
using aws console, cli, aws sdk 

#### 5. VPC Basics
- Remember, VPCs are specific to just a single region
- VPC acts as a network boundary
- it controls whole networking in cloud
- I as a customer get to define all of the subnetting
- i get to configure the routing table. where and what packet traverses through my aws account.
![alt text](image-6.png)
![alt text](image-7.png)
![alt text](image-8.png)
![alt text](image-9.png)

- default vpc
![alt text](image-10.png)

- Summary
![alt text](image-11.png)
![alt text](image-12.png)
![alt text](image-14.png)

#### EC2 instance type:
![alt text](image-15.png)

![alt text](image-16.png)



#### S3 Basics 
** S3 bucket names must be unique globally across all aws account.**
![alt text](image-17.png)
![alt text](image-18.png)
![alt text](image-19.png)


#### Route 53
- Aws managed dns service
- acts as a domain similar to sites like godaddy and namecheap
- is a global service and not specific to a region


#### AWS SDK
- doing everything through a code, below:
![alt text](image-20.png)

#### AWS Cloud Formationg
- cloud formation supports both json and yaml 
![alt text](image-21.png)

- Features
    - Iaac
    - Consistent and repeatable deployments
    - version control
    - Resource tracking
    - cost and time efficiency
    
- What is the role of a CloudFormation Stack Policy?
    -        prevent stack resources from being unintentionally updated or deleted during a stack update

''' aws cloudformation deploy --template-file s3-and-ec2.yaml --stack-name s3andec2stack --parameter-overrides S3BucketNameParameter=lambda-artifacts-948d01bc80800b36 '''


##### Deploy the cloudformation template file using cli
aws cloudformation create-stack --stack-name mys3andec2stack --template-body file://s3-and-ec2.yaml


## Iam roles:
create a role -> select trusted entity type (say, aws service, web identity) 

![alt text](image-23.png)


You have just terminated an EC2 instance in us-east-1a, and its attached EBS volume is now available. Your teammate tries to attach it to an EC2 instance in us-east-1b but he can't. What is a possible cause for this?
- ebs are locked to an AZ. but its possible to migrate them between different AZs using EBS snapshots.


You have launched an EC2 instance with two EBS volumes, the Root volume type and the other EBS volume type to store the data. A month later you are planning to terminate the EC2 instance. What's the default behavior that will happen to each EBS volume?

- By default, the Root volume type will be deleted as its Delete On Termination attribute is checked by default. Any other EBS volume types will not be deleted as its Delete On Termination attribute is disabled by default.

You can use an AMI in N.Virginia Region us-east-1 to launch an EC2 instance in any AWS Region. 
- NO
- AMIs are built for a specific AWS Region, they're unique for each AWS Region. You can't launch an EC2 instance using an AMI in another AWS Region, but you can copy the AMI to the target AWS Region and then use it to create your EC2 instances.

Which of the following EBS volume types can be used as boot volumes when you create EC2 instances?
- When creating EC2 instances, you can only use the following EBS volume types as boot volumes: gp2, gp3, io1, io2, and Magnetic (Standard).

What is EBS Multi-Attach?
- Using EBS Multi-Attach, you can attach the same EBS volume to multiple EC2 instances in the same AZ. Each EC2 instance has full read/write permissions.

You have provisioned an 8TB gp2 EBS volume and you are running out of IOPS. What is NOT a way to increase performance?
- For EBS gp2 volumes, it has max. IOPS of 16,000 or equivalent 5334 GB

You have a fleet of EC2 instances distributes across AZs that process a large data set. What do you recommend to make the same data to be accessible as an NFS drive to all of your EC2 instances?
- EFS is a network file system (NFS) that allows you to mount the same file system on EC2 instances that are in different AZs.

You would like to have a high-performance local cache for your application hosted on an EC2 instance. You don't mind losing the cache upon the termination of your EC2 instance. Which storage mechanism do you recommend as a Solutions Architect?
- EC2 Instance Store provides the best disk I/O performance.

You are running a high-performance database that requires an IOPS of 310,000 for its underlying storage. What do you recommend?
- You can run a database on an EC2 instance that uses an Instance Store, but you'll have a problem that the data will be lost if the EC2 instance is stopped (it can be restarted without problems). One solution is that you can set up a replication mechanism on another EC2 instance with an Instance Store to have a standby copy. Another solution is to set up backup mechanisms for your data. It's all up to you how you want to set up your architecture to validate your requirements. In this use case, it's around IOPS, so we have to choose an EC2 Instance Store.


