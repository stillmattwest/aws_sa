# Network Load Balancer (NLB)

NLBs work at Layer 4 (Transport), so TCP and UDP. 

They are much more performant than ALBs and can handle millions of requests per second.

NLB has one static IP per AZ and support assigning Elastic IP (helpful for whitelisting specific IP).

If you hear extreme performance, TCP or UDP, think NLB. 

Not included in the AWS free tier.

Like with the ALB, you associate an NLB with target groups.

The TGs can be EC2 instances or IP addresses, but the IPs have to be private.

It's also possible to layer load balancers and put an NLB in front of an ALB. 

NLB Health Checks support HTTP, HTTPS, and TCP.