---
created: 2024-07-21T19:03
updated: 2024-08-13T22:43
---
**Types of Storage:**
- Block Storage
- File Storage - network file system
- Object Storage - can be used in running instances - S3


**Performance Mode:**
- provisioned  mode -  fixed resources 
- on-demand/bursting mode - 

**EBS -  Elastic Block Store**
- volume attached to the EC2 instance
- root volume/adhoc volume that can be attached to ec2
-  EC2 and EBS should be in the same AZ

IOPS - Input/Output Operations Per Second
Input - Write
Output - Read

Volume Types in EBS:
- **General Purpose SSD (gp2)** - default volume type
- **Provisioned IOPS SSD (io1)** - high performance -  Multi attach  EBS volumes
- Provisioned IOPS SSD (io2) - latest version of io1
- General Purpose SSD (gp3) - latest version of gp2

**EFS - Elastic File System**
- shared file storage
- can be attached to multiple EC2 instances
- can be attached to multiple AZs
- can withstand the failure of an AZ 

**Pricing Plan in EC2:**
- On-demand - pay as you go
- reserved - 1 year or 3 year
	- Scheduled Reserved Instances - specific time period in a day 
- spot - bid the price 
- Savings Plan - commit to a consistent amount of usage
- Capacity Reservation - reserve capacity for specific instance type in a specific AZ
- Dedicated host - physical server dedicated to you

t2.micro, t3.micro, c4.large

- On-demand 
	- t2.micro instance  - per year $1000 
	- short term spikes
- Reserved 
	- t2.micro instance - per year $500 - upto 50% discount
	-  reserve the instance for 1 to 3 years
	-  on paying the upfront cost, the hourly rate will be reduced - max discount 65% discount
	-  unless the machine is in running state, the user is not charged for the instance/very minimal charge is charged
	-  usecase - in production environment, where the machine is running 24/7
- Scheduled Reserved 
	  -  reserve the instance for a specific time period in a day
	  -  usecase - batch processing
	  - in a day, need the instance only between 9AM to 6PM PST/EST
	  -  upto 75% discount
- Spot
	-  bid the price
    -  usecase - non-critical applications
    -  if the price is higher than the bid price, the instance will be terminated
    -  upto 90% discount
- Savings Plan
	- commit to a consistent amount of usage
	  -  usecase - production environment
	  -  200 hrs,  500 hrs
	  - ++ discounts
- Capacity Reservation
	-  1000 Core CPU, 100 TiB Storage, 10000 GiB RAM
	-  ++ discounts


**Autoscaling Group & Load Balancing in EC2:**

Load Balancer:
- Distribute the incoming traffic across multiple instances
- two types of load balancer - ALB and NLB
- Application Load Balancer  And Network Load Balancer

OSI Model:
- Application Layer - HTTP, HTTPS -  ALB
- Presentation Layer
- Session Layer
- Transport Layer - TCP, UDP - NLB
- Network Layer
- Data Link Layer
- Physical Layer


ASG - Autoscaling Group:

Min - 1
Desired - 3 <-- ASG listens to this value
Max - 10
3 instances are created


Min - 1
Desired - 0 <-- ASG listens to this value
Max - 10
?? instances are created


**Static IP in EC2 - Elastic IP address**


**Storage and Database Service in AWS:**

Object storage & s3 
database - SQL and NOSQL


**S3 - Simple Storage Service** -
- Object storage
- store and retrieve any amount of data
- store data in buckets

aws vs azure vs google cloud