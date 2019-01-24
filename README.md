# quickstart-portworx

https://portworx.com/

<img src="images/portworx-logo.png" alt="drawing" width="100"/>

# What is Portworx

Portworx is the solution for running stateful containers in production, designed with DevOps in mind. With Portworx, users can manage any database or stateful service on any infrastructure using any container scheduler, including Kubernetes, Mesosphere DC/OS, and Docker Swarm. Portworx solves the five most common problems DevOps teams encounter when running stateful services in production: persistence, high availability, data automation, security, and support for multiple data stores and infrastructure.

# Features

## Data Mobility

Backup, recovery, migration made easy

To be useful, containers must be portable. But data has gravity, and moving a stateful app like a database between servers, let alone data centers is a challenge not addresses natively by container platforms. Thanks to PX-Motion™, Portworx makes your data as portable as your stateless containers, making the promise of multi- and hybrid-cloud computing a reality.

## High Availability

HA for all of your databases and stateful containers.

When a server fails, your database container can fail with it. Mitigating failure with custom hardware is expensive (not to mention anti-DevOps), while database-driven replication can be time-consuming and impact performance, especially as the cluster rebuilds.

### Container-Granular Replication

With Portworx, your scheduler of choice + our container-granular replication mean that losing a node or disk in your cluster doesn’t mean downtime or degraded performance.

### Multi-AZ by Default

Portworx’s persistent storage layer automatically spans hardware racks and availability zones so you can run databases and stateful applications uninterrupted by hardware failures and public cloud outages.

### Smart Provisioning

Portworx aggregates servers, SANs, and clouds to create a unified persistent storage layer for database containers or other stateful containers, tiering across class-of-service, IOPS, and availability zones. Your
apps will be automatically deployed on the best storage for their performance and capacity needs.

## Scheduler Based Automation

Manage your data layer with Kubernetes

Your DevOps team can’t wait days or weeks for container volume storage provisioning just to deploy their applications. Portworx makes your stateful containers as easy to deploy and manage as the stateless parts of your app.

## Data Security

Move fast. Move securely.

Managing data comes with special requirements, from specific regulatory issues to simply maintaining customer trust. Portworx lets you move at DevOps speed while maintaining your apps’ security requirements.

### Encryption

Portworx provides highly secure, key-managed encryption for container volumes that integrates with popular key management systems like AWS KMS and Hashicorp Vault. Encryption can be applied to any application and is independent of the cloud infrastructure.

### Access Controls

Portworx provides access controls and security for data at rest as well as data in flight. Move fast, but move securely.


## Data Protection

Portworx provides consistent snapshots, 3D application-aware snapshots and cloudsnaps to Amazon S3

# Why Potworx + AWS?

EKS and Portworx are a match made in heaven. The best storage for Kubernetes. Period.

Running stateful services on Kubernetes is fraught with peril–stuck volumes, downtime, manual backups and migrations, lost data. Portworx solves these challenges and more with cloud native storage and data management built from the ground up for Kubernetes.

When you use Portworx as the data management layer for Kubernetes, you can:

- Reduce time-to-market for container projects dramatically
- Reduce compute costs by 40-60%
- Reduce storage costs by 30% or more
- Reduce ops and support costs by millions annually

# How to use

Use `portworx-master.template.yaml` as a way to get started from scratch and `portworx-master-existing-vpc.template.yaml` if you already have a VPC.

Provide the following

- KeyPairName
- RemoteAccessCIDR
 
Provide more detail or accept the defaults. 

The following are available to configure Portworx

- PortworxVersion
- LightHouseVersion
- VolumeTemplateString

## Deploy databases

Use the templates available in `examples/` directly to easily launch Databases onto EKS using Portworx.
