---
created: 2024-09-28T18:38
updated: 2024-09-28T21:09
---

delete container - docker, docker compose - cannot bring it back 
manually restart the container

AWS - EKS - Elastic Kubernetes Service
Azure - AKS - - Azure Kubernetes Service
GCP - GKE - - Google Kubernetes Engine
OCI - OKE -- - Oracle Kubernetes Engine


Kube Controllers:
- ReplicaSet
- Deployment
- StatefulSet
- DaemonSet
- Job

Kube Scheduler:

-> will override the expose port in docker

service in kubernetes
- clusterIP - private IP - default
- nodeport - node ip address to access pod
- loadbalancer - aws load balancer to route traffic to pod


when you create nodeport, clusterip is created by default
when you create load balancer, nodeport is created. 
