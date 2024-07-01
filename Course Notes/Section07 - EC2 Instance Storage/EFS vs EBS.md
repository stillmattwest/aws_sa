# EBS vs. EFS

**EBS Volumes**

* One instance (except multi-attached io1 and io2 types)
* Are locked to one AZ
* gp2: IO increases as disk size increases
* gp3: IO can increase independently

To Migrate an EBS Volume across AZs
* Take a snapshot
* Restore the snapshot to another AZ
* EBS backups use IO and we shouldn't run them while the application is handling traffic

Root volumes of EC2 instances get terminated by defualt if the instance is terminated. This can be disabled.

**EFS File System**

* Mounting 100s of instances across AZs
* EFS Share Websites files
* Only for Linux instances (POSIX)
* EFS is more expensive than EBS
* Can leverage storage tiers for cost savings
* Remember EFS vs EBS vs Instance Store (see notes)