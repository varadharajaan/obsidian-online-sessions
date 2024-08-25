---
created: 2024-08-24T20:34
updated: 2024-08-25T22:16
---

before automation - manual setup knowledge is required


LAN - Lan area network
WAN
topologies - bus,star, mesh

internet - all machines across the globe is connected with each other

IP - internet protocol




IPv6 - skip this
128 bits
hexadecimal ( alphanumeric)
ads1232123::asdasd12e321g::3423dsfdfsf::sdfsdf23234gds

IPv4 - 32 bits

00000000.00000000.00000000.00000000  ~ 0.0.0.0

11111111.11111111.11111111.11111111 ~ 255.255.255.255

0 to 255

23.24.1.4 - valid ip - yes
245.23.1.3 - valid ip - yes
<font color="#c0504d">256</font>.2.4.200 - valid ip - no

class A  - 1 to 126
class B - 128 to 191
class C - 192 to 223

--------------
class D - 224 to 239 - govt and research purpose
class E - 240 to 255




CIDR range - classless inter domain routing

**10.0**.0.0/**16**
32 bits
first **<font color="#000000">16</font> bits** are fixed for network - cannot be changed
last 16 bits are for host - can be changed


120.0.0.0/20
first 20 bits  are fixed for network - cannot be changed
remaining 12 bits can be changed for host

VPC - virtual private cloud/ Virtual network/ Vnet
10.0.0.0/16 - 256 subnets * of 256 ips = 65536 ips ( servers, databases, etc)

10.0.0.0
10.0.0.1
10.0.0.2
.
.
10.0.0.255 - 256 ips

first 24 bits are fixed
last 8 bits changing 


CIDR - 10.0.0.0/24




10.0.1.0
10.0.1.1
10.0.1.2
.
.
10.0.1.255 - 256 ips

CIDR - 10.0.1.0/24


10.0.2.0
10.0.2.1
10.0.2.2
.
.
10.0.2.255
CIDR - 10.0.2.0/24
.
.
.

10.0.255.0
10.0.255.1
.
.
10.0.255.255

CIDR - 10.0.255.0/24


inbound traffic  - incoming traffic / ingress
outbound - outgoing /egress


private IP - internal communication
public IP  - internet access

for internet access:
1. public IP for the machine
2. gateway - internet gateway (IGW) for the virtual network
3. deploy route table to the subnet and add route to gateway

0.0.0.0/0 -> IGW is called public route
public route table

when public route table is assigned to subnet, subnet is called public subnet


Instance level firewall - security group
blocks all traffic - by default


subnet level firewall - NACL ( (network access control list)

VPC or regional level firewall - WAF ( web application firewall)

Bastion Server
jump box
jump server


auto scaling in AWS / VMSS - virtual machine scale set 
load balancer in AWS
database in AWS

network packets transfered
request count
storage IOPS - input output processing per second < 1000

backend pool 

95% - deploy at least in 2AZ
95 - 99% - more than 2AZ
more than 99% - DR - disaster recovery

95% - $200
99% - $500
99.99% - $800
99.999% - $1000


launch template - pre defined template with all configurations
ami
instance type
key pair
sec group
network
storage
what application to be deployed - mongodb, mysql

bootstrap script or userdata - script to be executed when instance is launched
```bash
#!/bin/bash
# Use this for your user data (script from top to bottom)
# install httpd (Linux 2 version)
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
echo "<h1>Hello World from $(hostname -f)</h1>" > /var/www/html/index.html


ASG
min  - 1
desired - 0 <-- ASG
max - 5