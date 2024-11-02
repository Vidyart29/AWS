# cloud-computing

### Before Cloud Computing
Before cloud, every company had there individual data center i.e there own servers, which does very fast processing in very less time. (huge storage capacity, etc..)
and all these servers where housed in a datacenter, so that all the employees working could connect to it, and for the connection they use to connect to vpn first and then with the ISP. 


### AWS vs Azure vs GCP Service Comparison

- Compute services

Service | AWS | Azure | GCP         
------------ | ------------- | ------------- | ------------- 
Virtual servers | Elastic Compute Cloud (EC2) | Virtual Machines | Compute Engine
PaaS, deploying apps | Elastic Beanstalk AWS Lightsail | Azure App Service | App Engine Environment
Autoscaling | Auto Scaling | Azure Autoscale VM Scale Sets | Autoscaling
VMware Cloud | VMware Cloud on AWS | Azure VMware Solution | VMware Cloud on GCP


- Container services and serverless computing

Service | AWS | Azure | GCP         
------------ | ------------- | ------------- | ------------- 
Managed container services	| EC2 Container Service (ECS) Amazon Kubernetes Service (EKS) |	Azure Container Service (AKS)	| Google Kubernetes Engine
Docker container registry	| Elastic Container Registry (ECR) | Container Registry	| Container Registry
Serverless container services| 	AWS Fargate | 	Azure Container Instances (ACI) | Google Cloud Run
Serverless/Function-as-a-Service |	AWS Lambda | Azure Functions | Google Cloud Functions


- Storage services

Service | AWS | Azure | GCP         
------------ | ------------- | ------------- | ------------- 
Object storage |	Simple Storage Service (S3) |	Azure Blob Storage |	Google Cloud Storage
Block storage	| Elastic Block Store (EBS) |	Azure Disk Storage |	Google Persistent Disks
Infrequent access/archive storage |	S3 Glacier Deep Archive S3 Infrequent Access |	Azure Archive Storage Azure Cool Blob Storage	 | Google Cloud Storage Nearline, Coldline, and Archive
File storage| 	Elastic File System (EFS) |	Azure Files	Google | Cloud Filestore
Bulk data | transport	AWS Import/Export Service AWS Snow Family	| Azure Import/Export Service Azure Data Box  |	Storage Transfer Service
Backup storage |	AWS Backup|	Azure Backup |	Google Cloud Storage
Disaster recovery |	Disaster Recovery | Disaster Recovery Cookbook |	Site Recovery


- Database services

Service | AWS | Azure | GCP         
------------ | ------------- | ------------- | ------------- 
Managed relational database as a service | Amazon RDS |SQL Managed Instances | Cloud SQL
With serverless options |	Amazon Aurora	| Azure SQL Database | Cloud Spanner
No SQL database as a service | Amazon DynamoDB | Azure Cosmos DB | Cloud Bigtable
In-Memory database services	| Amazon ElastiCache|	Azure Cache for Redis|Memorystore
Document database services | DocumentDB	| Azure Cosmos DB	 | Filestore
Data warehouse services	| Amazon Redshift |	Azure Synapse |	BigQuery
Data analysis services |	Amazon Athena| 	Azure Synapse	| BigQuery
Ledger services	| Amazon QLDB |	Azure Workbench	| Cloud Spanner
Graph database services| 	Amazon Neptune| 	Neo4j (Azure Partner)	| Cloud Bigtable


- Network services

Service | AWS | Azure | GCP         
------------ | ------------- | ------------- | ------------- 
Global Content Delivery Networks (CDN)	| Amazon CloudFront | 	Azure Content Delivery Network (CDN) | Google Content Delivery Network (CDN)
Direct connection |	AWS Direct Connect |	Azure ExpressRoute	| Google Cloud Interconnect
DNS |	Amazon Route 53 |	Azure DNS Traffic Manager |	Google Cloud DNS
Load balancing | 	Elastic Load Balancing (ELB)| 	Azure Load Balancer Application  Gateway |	Cloud Load Balancer
Virtual private cloud network | 	Virtual Private Cloud (VPC)	| Virtual Networks (VNet)	| Google Virtual Private Cloud (VPC)


- Cloud security services

Service | AWS | Azure | GCP         
------------ | ------------- | ------------- | ------------- 
Authentication and authorization |	Identity and Access Management (IAM) | Azure Active Directory | Google Cloud Identity and Access Management (IAM)
Web firewall |	AWS Web Application Firewall |	Azure Application Gateway Azure Firewall	 | Firewall Insights
Security assessment	| Amazon Inspector AWS Security Hub	| Azure Security Center| 	Cloud Security Command Center
Threat detection and monitoring |	Amazon GuardDuty |	Azure Advanced Threat Detection |	Cloud Armor










