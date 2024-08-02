---
created: 2024-07-16T09:22
updated: 2024-08-02T16:35
---

horizontal scaling

increase or decrease the instance quantity

scale in - remove instance
scale out - add instance


vertical scaling

increase or decrease the size of the machine

scale up - increase the instance size
scale down  - decrease the size


Cloud Deployments:

1. availability
2. scaling
3. pay as you go
4. security 
5. global deployments in easy in cloud



AWS AZURE GCP


100 GiB/sec - network 
AWS - $500 per hour
Azure - $620 per hour

GCP - $100 per hour


**Azure  Cloud:**

1. networking
2. compute resources
3. storage
4. database  ~~


Azure Offerings
1.  Tenant 
2. subscription
3. Resource group


**Azure Virtual Machines:**

processing unit
CPU 
RAM
storage
network - configurable
OS




Azure UserData:

Inbound traffic - incoming traffic the server
outbound traffic - outgoing traffic

ingress
egress


0.0.0.0/0

CIDR - /16 /20



Azure UserData:

bootstrap script during server startup


Azure Image:


VMSS - virtual machine scale set



**VM Pricing**:

Pay-as-you-go (On-demand) - costlier among others
- $100 per year for b2s instance
Reserved/Scheduled Reserve - 1 to 3 years. 
- discount upto 50% of actual pricing (ondemand)
- $50 dollars per year
- ++ discounts for upfront
- Scheduled Reserve  - 5PM to 9PM in a day for 1 year/3 years
- upto 70% discount
Spot instance
- upto 90% discount
- 2 mins grace time notification.
- backuptime - ??
- 1000 cores, 10,000 GiB RAM - reservations aka capacity reservation

VMSS  - virtual machine scale set ( auto scaling )
load balancer 
OSI model - 7 layers

**application layer - layer 7** 
presentation layer
session layer
**transport layer - layer 4**
network layer
data link layer
physical layer


SSL termination -> HTTPS to HTTP
NAT - network translation ( proxy)


Load balancer in Azure:
- app gateway - layer 7 
- load balancer - layer 4 and layer 7 
- traffic manager - DNS load balancing cross regional/global
- front door - DNS + cache ( Content delivery network)


VMSS

min count -  1
**desired count - 5 <-- VMSS**
max count - 10
5 instances

min count -  1
**desired count - 0 <-- VMSS**
max count - 10
1 instance

min count -  1
**desired count - 50 <-- VMSS**
max count - 10

chmod 400 demo_key.pem - works in bash terminal



















