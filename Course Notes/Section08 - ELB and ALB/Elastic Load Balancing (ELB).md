# ELB: Elastic Load Balancing

## What is Load Balancing?

Basic stuff, but a load balancer is a server that sits between your users and multiple instances of your application. The load balancer associates a given user with a given instance, and it spreads users out between instances dynamically using some type of algorithm. 

The user has no idea which instance of your app they're connected to, it all happens behind the scences. 

Load Balancers can:

* Spread load across multiple downstream instances

* Expose a single point of failure for downstream instances

* Handle downstream failures

* Perform regular health checks of your instances

* Provide SSL termination for your websites

* Enforce stickiness with cookies

* Allow high availability across zones

* Separate public from private traffic

## Elastic Load Balancer (ELB)

ELB is the AWS implementation of a load balancer. It costs a bit more than building your own LB, because it is a managed service.

ELB is the way to go for the vast majority of apps. AWS guarantees the ELB will be working, handles all upgrades and maintenance, and provides a few configuration options.

ELB integrates with many relevant AWS services including EC2, auto-scaling groups, CloudWatch, etc. 

## Health Checks

Health Checks are crucial for load balancers. The health check is against an EC2 instance such as a web server and is done on a port and a route. `/health` is a common route. 

If the EC2 instance does not send a 200 response to the check, then the instance is unhealthy and the ELB will not send traffic to it. 

## Types of Load Balancers

AWS has four types of LBs:

* Classic Load Balancer 
    * Supports HTTP, HTTPS, TCP, SSL
    * Deprecated
* Application Load Balancer
    * HTTP, HTTPS, WebSocket
* Network Load Balancer
    * TCP, TLS (secure TCP), UDP
* Gateway Load Balancer
    * Operates at Layer 3 (IP layer)

Some load balancers can be setup as internal or external ELBs. 

## Load Balancer Security Groups

The ELB can act as a gateway of sorts, and should be in its own security group. Look at it as something outside the firewall (A DMZ).

The Application Security Group should *only* accept HTTP or HTTPS traffic from the ELB. Any other traffic gets dropped. 


