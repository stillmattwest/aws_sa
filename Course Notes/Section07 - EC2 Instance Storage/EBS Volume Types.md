# EBS Volume Types

EBS Volumes Come in Six Different Types:

* gp2 / gp3: General Purpose SSD volume. Balances price and performance.
* io1/io2: Highest performance SSD. Low latency.
* st 1: An HDD volume but high throughput
* sc 1: A low-cost HDD for less frequently accessed workloads.

EBS Volumes are characterized by three metrics:

* Size
* Throughput
* IOPS (I/O Operations Per Second)

For EC2 Instances, only gp2/gp3 and io1/io2 can be used as boot volumes.

## General Purpose SSD

Cost effective, low-latency storage.

Good for system boot volumes, virtual desktops, dev and test environments.

1 GiB (1 GiB = 1.074 GB) to 16 TiB

gp3:
* Baseline of 3,000 IOPS and throughput of 125 MiBs.

* Can increase IOPS up to 16,000 and throughput up to 1000 MiB/s independently.

gp2:

Older standard. Small volumes can burst IOPS to 3,000.

Size of volume and IOPS are linked. +3 IOPS per GB. Takes 5,334 GB of size to max IOPS. 

## Provisioned IOPS

This is the EBS volume types for critical business applications with sustained IOPS performance.

Great for database workloads, and that's a keyword to watch out for in the exam.

io1 has 32,000 to 64,000 IOPS. The 64K is for Nitro EC2.

io2 has sub-milisecond latency and 256,000 IOPS or PIOPS (provisioned IOPS)

io2 supports EBS multi-attach.

## HDD Types

st1 and sc1.

Cannot be a boot volume.

125 GiB to 16 TiB.

