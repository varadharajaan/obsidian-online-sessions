---
created: 2024-07-17T09:16
updated: 2024-08-02T16:35
---

types of offerings in cloud:
IAAS - infra as a service
PAAS - platform as a service - java, .net - App service.
SAAS - software as a service -  azure functions


App service:
App Service Plan - 

Visual studio

Trigger -> 

2mins times out automatically

file size 

database
cache


**Storage Account in Azure:**\

block storage - disk

storage account
object storage -  blob storage, AWS - s3 - public internet
file storage - NFS
queue storage


IOPS - input output processing per second
5000

Block Storage:

azure managed 
manual backup 


LRS 
ZRS
GRS
GZRS


IOPS - 10,000


https://demostorage3e23.blob.core.windows.net/demo/custom_image.txt



SAS token - shared access token container/file
access key - storage account level


https://demostorage3e23.blob.core.windows.net/demo/custom_image.txt


  
https://demostorage3e23.queue.core.windows.net/demoqueue


hot storage -
cold storage


life cycle:

1- 180 days - hot storage - 10GiB $2

180 - 300 - cool - $1 

300 - 400 days - cold - $0.5

3 years - archive - 6 hrs

10 tiers - delete

Upsert command - insert or update

**Azure Database service:**

DBAAS - database as a service

SQL  - consistency 


NOSQL  - 

CAP theorem - 

CA - SQL
AP - couchbase, mongodb
PC - IBM db2 

eventual consistency
strong consistency - 90% 100% 50%



MYSQL DB
postgres 
MSSQL


Cosmos DB - global distribution nosql database in azure

RU - read unit
WU  - write unit -  300 units 

TTL - time to alive 


**Azure Networking:**

Virtual Network:

CIDR - classless inter domain range


23.45.34.1 - valid


245.240.2.**300** not valid


23.2.1.1/32

Vnet
10.0.0.0/**16** - 256 * 256 ips = 65256 ips

first **16** bits are fixed - dedicated to network & cant be changed
remaining 16 bits are host machines - can be changed 

subnets
24 bits are fixed
last 8 bits changing
CIDR  - 10.0.0.0/24
10.0.0.0
10.0.0.1
10.0.0.2
.
.
10.0.0.255 - 256 ips


CIDR - 10.0.1.0/24
10.0.1.0
10.0.1.1
.
.
10.0.1.255


CIDR - 10.0.2.0/24
10.0.2.0
10.0.2.1
10.0.2.2
.
.
10.0.2.255


.
.
.

CIDR - 10.0.255.0/24
10.0.255.0
10.0.255.1
.
.
10.0.255.255




 public IP
 route table - routing to internet
IGW - internet gateway


class A - 0 to 100
B C 10 to 120 

----------
D
E

120.0.0
10.0.0
20.0.0


app.com

geo.app.com  - 120.0.0.0 140.0.0.0
routing policy - geolocation, weighted policy,  failover policy, latency policy


US - us ip

120.0.0.0
255.255.255.0

nameservers


policy

IAM - identity access management








 
















INTERNET

INTRANET - topologies,  WAN LAN


IPV4 - 32 bits

00000000.00000000.00000000.00000000 ~ 0.0.0.0

11111111.11111111.11111111.11111111 ~ 255.255.255.255

0.0.0.1

10.23.45.244












------
IPv6 - 128 bits
hexadecimal
alphanumeric


23nlk2jasdasf::asdf232dfsfdsfs::asda2312312


























