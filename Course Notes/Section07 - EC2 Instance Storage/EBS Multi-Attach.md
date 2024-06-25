# EBS Multi-Attach

The use case here is to attach multiple EC2 instances to a single high-performance EBS.
This is important for clustered Linux applications like Teradata.

Also handles concurrent write ops.

Can take up to 16 EC2 instances at a time.

Must use a file system that is cluster aware, so NOT XFS or EXT4.

Only works with io1 or io2 EBS types.

