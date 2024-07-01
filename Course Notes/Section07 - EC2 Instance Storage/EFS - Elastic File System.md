# EFS - Elastic File System

EFS is a managed Network File System (NFS) that can me mounted on many types of EC2 instances.

EFS volumes are highly available and scalable but they are also expensive. 3x the cost of a typical EBS volume.

The big advantage of EFS volumes is they can be used by EC2 instances across AZs. All EC2 instances attached to the EFS can access it simultaneously.

## EFS Fact Sheet

* Use cases: content management, web serving, data sharing, Wordpress
* Uses NFSv4.1 protocol
* Must be inside a security group to control access
* Compatible with Linux but not Windows
* Encryption at rest using KMS
* POSIX file system (Linux) w/ standard file API
* Scales automatically. Pay-per-use, no capacity planning

## Use Case Example

Let's say you took a project for a company with a big WordPress site (or another CMS site). That needs to be installed, so you'd install it to an EFS volume, and then mount that volume to as many EC2 instances as you needed for load balancing. Meanwhile, you use S3 and Cloudfront to host your images and media and RDS to host your database. 

This gives you a scalable solution and you can use cross-region replication to achieve low latency for customers world wide.

## EFS Performance Classes
* EFS Scale
    * 1000s of concurrent NFS clients, 10 GB throughput
    * Grow to petabyte scale automatically

* Performance Mode (set at EFS creation)
    * General Purpose (default): latency sensitive use cases (web server, CMS, etc)
    * Max I/O: higher latency, highly parallen (big data, media processing)

* Throughput Mode
    * Bursting 1TB = 50 MiB/s + burst up to 100MiBs
    * Provisioned: set throughput regardless of storage size
    * Elastic: Automatically scale throughput based on workloads. Up to 3GiBs for reads and 1GiBs write.


## EFS Storage Classes

Storage Tiers

* Standard: for frequently accessed files
* Infrequent Access (EFS-IA): lower price to store, but there is a cost to retreive files
* Archive: rarely accessed (few times per year) data. 50% cheaper storage.

We implement *lifecylce policies* to automate moving files between storage tiers.

Availability and Durability

* Standard: Muti-AZ, great for prod
* One Zone: One AZ. Great for dev. Backup enabled by default. Compatible with IA (EFS One Zone IA).
* Over 90% cost savings


