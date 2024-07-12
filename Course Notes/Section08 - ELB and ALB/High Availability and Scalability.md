# High Availability and Scalability

Scalability is an attribute that allows applications to adapt to increased load. There are two kinds of scalability: vertical and horizontal. The term elasticity refers to horizontal scalability. 

## Scalability

Scalability is linked to high availability but not synonymous. 

Vertical scalability means increasing the size of the instance. 

Horizontal scalability means adding additional instances and distributing the load across instances.

Vertical scalability is common with databases.

## High Availability

The goal of high availability is to survive a data center loss. It means running your system or application in at least two separate AZs (e.g., data centers).

High availability can be passive or active. 

## Auto-Scaling and Load Balancing Groups

For horizontal scaling, use an auto-scaling group and a load balancer.

For high availability, use multi-AZ versions of auto-scaling groups and load balancers. 

