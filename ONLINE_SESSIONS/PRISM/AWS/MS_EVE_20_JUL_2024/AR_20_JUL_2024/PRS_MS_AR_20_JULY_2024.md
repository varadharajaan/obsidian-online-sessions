---
created: 2024-07-20T12:26
updated: 2024-07-20T22:18
---
**CLOUD COMPUTING:**
Pay-as-you-go model for computing resources. 
On-demand delivery of IT resources and applications via the internet with pay-as-you-go pricing.
cloud providers offer services such as computing power, storage, and databases.
- [ ] **AWS** - Amazon Web Services
- [ ] **GCP** - Google Cloud Platform
- [ ] **Azure** - Microsoft Azure
- [ ] **IBM Cloud** - IBM Cloud

setup the own server
rent the server from the cloud provider

- [ ] **IaaS** - Infrastructure as a Service
- [ ] **PaaS** - Platform as a Service
- [ ] **SaaS** - Software as a Service

Datacenter: - physical location to store servers and network equipment. 
- [ ] **On-premises** - own datacenter
- [x] **Colocation** - rent space in a datacenter
- [ ] **Cloud** - rent servers from a cloud provider

Scaling - increase or decrease the resources based on the demand
- [ ] **Vertical Scaling** - increase the resources of a single server
- [ ] **Horizontal Scaling** - increase the number of servers

**Onprem datacenter:**
- [ ] **CapEx** - Capital Expenditure
- [ ] **OpEx** - Operational Expenditure
- [ ] Scaling & Elasticity - limited
- [ ] Disaster Recovery - manual
Elasticity - ability to increase or decrease the resources based on the demand

**Cloud Datacenter:**
- maximum scaling & elasticity
- Availability - 99.99% 
- Disaster Recovery - automatic
-  3000 core CPU & 30,000 GiB RAM in one machine

**when not to goto cloud:**
- **Regulatory Compliance** - data should be stored in a specific location
- **Security** - PII and sensitive data
- **Cost** - if the cost is high, 1000 

**AWS  - Amazon Web Services**

**AWS Global Infrastructure:**
- 24 regions
- 77 availability zones -  AZ
- 220 countries

to create a server in AWS, need to choose the **region** and **AZ**

EC2 - Elastic Compute Cloud aka Virtual machine 

Laptop:
- OS
- CPU & RAM & GPU - 4 core CPU, 16 GiB RAM etc
- Storage
- Network - WiFi, NFC , Bluetooth

components of EC2:
Instance Type & Family:
- General Purpose
- Compute Optimized - latest CPU and clocked CPU
- Memory Optimized  - latest DDR5 RAM
- Storage Optimized - SSD, NVME, 15 TiB SSD
- Accelerated Computing - GPU, FPGA, TPU
- HPC Optimized - High Performance Computing

most used ports in EC2:
- 22 - SSH
- 80 - HTTP
- 443 - HTTPS
- 3389 - RDP

default firewall in EC2 - Security Group blocks all the incoming traffic

run automated script in ec2 during the startup - bootstrap script or user data

AMI - Amazon Machine Image - OS + software
- amazon defined AMI
- user defined AMI
Visibility - public, private, shared
private - only the owner can see
shared - shared with other AWS account

