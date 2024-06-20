# AMI Overview

AMI = Amazon Machine Image

An AMI is an image of a customized EC2 instance. They are used to enable quick launching of an EC2 instance with a certain combination of OS, installed software, monitoring, etc. 

This obviously reduces setup time considerably.

AMIs are built for a specific region and can be copied across regions.

You can launch EC2 instances from:
* A public AMI that AWS provides. The Amazon Linux 2 AMI is a popular one.

* Your own AMI. Make and maintain them yourself.

* A third-party AMI from the AWS marketplace. These AMIs come prepackaged with vendor software, usually configured in a nice way. AMI images can be free or purchased depending on the vendor.

## AMI Processes

* Start an EC2 instance and customize it
* Stop the instance
* Build an AMI from the instance. This will also create EBS snapshots.
* Launch instances from the AMI.

