# EC2 Placement Groups

EC2 placement groups are used to control the EC2 instance placement strategy. 

There are three available strategies:

* Cluster: clusters instances into a low-latency group in a single AZ.
* Spread: spreads instances across underlying hardware (max 7 instances per group per AZ). Good for critical applications.
* Partition: Spreads instances across many different partitions, which rely on different sets of racks within an AZ. Scales to 100s of EC2 instances per group. Use cases include Hadoop, Cassandra, and Kafka.

## Cluster Placement Group

Pros: Great networking. 10Gbs.

Cons: If the AZ fails, all instances die.

Use Case: Big Data jobs that need to complete quickly. Any application that needs fast networking.

## Spread Placement Groups

Pros: All EC2 instances are on different hardware. Can even span across multiple AZs. Reduced risk of simultaneous failure. EC2 instances are on different physical hardware.

Cons: Limited to 7 instances per AZ per placement group.

Use Case: Application that needs to maximize high availablity.

## Partition Placement Group

Pros: EC2 instances are spread across multiple partitions, which are each on a separate physical rack within an AZ. Allows up to 7 partitions, and 100s of individual EC2 instances. 

Instances in one partition do not share hardware with instances in another partition.

Use cases are mostly for big data. 



