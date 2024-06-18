# EBS Overview

EBS = Elastic Block Store.

EBS "instances" are called volumes. As if you attach an EBS volume to an EC2 instance.

This is a networked HDD or SSD that we can attach to an EC2 instance.

It exists independently of the EC2 instance, so it allows us to persist data even if we terminate an EC2 instance that was using it.

It is possible to mount an EBS volume to multiple EC2 instances, but this is a more advanced operation.

Free Tier: 30GB of free EBS storage of type General Purpose (SSD) or magnetic per month.

## EBS Basics

* EBS Volumes are network drives, not physical drives. They have a bit of latency.
* EBS volumes can be detached from one EC2 instance and attached to another very quickly. Great for failover.
* EBS volumes are locked to one AZ.
* Snapshots, however, can be moved between AZs.
* EBS volumes have a provisioned capacity, both in size (GBs) and IOPS (I/O Per Second).
    * Billing is based on that capacity, not what you're actually using
    * It is possible to increase the capacity of an instance if you need more

## Delete on Termination Attribute

While EBS volumes persist after their EC2 instance is terminated by default, it is possible to set a Delete on Termination attribute in the console, which will cause the EBS to terminate along with the EC2 instance.

The root EBS is by default set to delete on terminate. Any additional EBS volumes are NOT set this way. 

We can also deselect this option from the root volume. This might show up in the exam.



