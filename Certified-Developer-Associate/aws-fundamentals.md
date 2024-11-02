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

