# Elastic Network Interfaces (ENI)

A logican component in a VPC that represents a virtual network card.

Each ENI can have the following attributes:

* Primary private IPv4, one or more secondary IPv4

* One Elastic IP (IPv4) per private IPv4

* One public IPv4

* One or more security groups

* A MAC Address

You can create ENI independently and attach them on the fly (move them) on EC2 instances for failover.

ENIs are bound to a specific AZ.

ENIs are available in the console in the EC2 dashboard via the networking section.