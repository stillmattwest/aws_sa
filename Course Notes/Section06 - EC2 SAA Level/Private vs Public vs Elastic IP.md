# Public vs. Private vs. Elastic IP

Private and Public IPs are the same in AWS as they are everywhere.

## Elastic IPs

Elastic IPs are public IP addresses that you own as long as you don't delete it. They can be attached to instances, but obviously only one instance at a time. 

Without an Elastic IP, EC2 instances will change their public IP address whenever you stop and start them.

You can only have five elastic IPs in your account. 

**Using an Elastic IP is usually considered a poor architectural decision.**

Instead, use DNS and point it to an AWS network.

