---
created: 2024-07-20T12:26
updated: 2024-07-20T16:19
---
DRIVE LINK - [BATCH_WE_AWS_MASTER_20_JUL_2024](https://1drv.ms/f/s!Aq4Ajy5pKSh3hLEfcLbdT9mm7W1YeA?e=7XrQjU)

basic 50+ most used commands in Linux

**Cloud Computing:**
- various service offering over the internet
- on-demand/pay-as-you-go service 
- remotely/virtually accessible.
- providers - AWS,Azure,GCP,OCI,BlueMix etc

**Datacenter: (DC)**
- storage/server deploy locations.
- Virtual machine/Host instance & storage & networking & databases

**Self-managed DC:**
- users manage themselves, Servers, DB, Storage, networking etc
- time & cost - at initial stage - HIGHER
- elasticity & scalability of the application - restricted

**Cloud-Managed DC:**
- AWS, Azure, GCP like clouds manage the DC and rent the servers, storage etc on pay-as-you-go model
-  300 core CPU and 7000 GiB RAM - max spec of 1 machine
-  scaling is easy and resources are always available on-demand usage

**Scaling of virtual machines:**
- Vertical scaling
    -  increase or decrease the size of the machine
    - Scale up - increase and scale down - decrease
- horizontal scaling
	- add or remove the compute instances
	- scale in - remove the instance and scale out - add instance

**Why not Cloud:**
- security - we use someone else computer/machine
- GDPR concerns - 
-  long term cost - ~ 10 years
-  License for servers and other applications for on-prem ~ 1000+ licenses

**AWS - Amazon Cloud Services**
major resources:
1. compute 
2. storage
3. database
4. networking
5. Security and IAM
many more managed services.

**Regions and Availability zones in AWS**

Regions - group of AZ
AZ - Availability zone - Cluster of DCs

**1.Compute Services in AWS**

Servers/Virtual Machines

CPU
RAM
Storage

16 GiB RAM, 8 core CPU
32 GiB RAM, 16 core CPU, 8 GiB GPU
Linux
Windows
Mac

**Instance Type and Instance Family**

EC2 - Elastic Compute Cloud
Server/Virtual machines etc

OS - AMI
CPU
RAM
Storage
\
Key pair
public key
private key


Firewall 

**Build your own desktop:**

SSH - port 22
HTTP - port 80
HTTPS - port 43
RDP - port 3389


bootstrap script - script to be run during server startup
userdata script
