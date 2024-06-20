# EC2 Instance Store

EBS volumes are network drives with good but limited performance. 

If you need a high-performance hardware disk, use EC2 Instance Store.

The difference is that an Instance Store is physically connected to the server. 

* Better I/O performance
* EC2 Instance Stores lose their storage if they're stopped (ephemeral storage). 
* Good for bugger/cache/scratch data or other temporary content.
* Risk of data loss if hardware fails
* Backups and Replication are the user's responsibility


