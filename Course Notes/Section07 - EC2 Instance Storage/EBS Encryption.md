# EBS Encryption

When you create an encrypted EBS volume the data is encrypted at rest within the volume, and in-flight between the volume and the EC2 instance. All snapshots and any volumes created from them are also encrypted.

Encryption has a very minimal impact on latency, almost nothing. 

EBS encryption leverages keys from KMS (AES-256).

Copying an unencrypted snapshot allows encryption.

## How to Encrypt an Unencrypted EBS Volume

You kind of can't, but there is a workaround.

* Create an EBS snapshot of the volume
* Encrypt the EBS snapshot using copy
* Create a new EBS volume from the snapshot (which will also be encrypted)
* Attach the encrypted volume to the original instance. 

