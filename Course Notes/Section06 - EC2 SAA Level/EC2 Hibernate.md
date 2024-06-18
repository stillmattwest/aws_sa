# EC2 Hibernate

*Review: EBS = Elastic Block Storage. It's SSD storage attached to an EC2 instance.*

On Starting, Stopping, and Terminating instances:

## Stopping and Terminating
* Stop: the data on disk (EBS) is kept intact until the next start.
* Terminate: Any EBS volumes (root) also set up to be destroyed is lost.

## Starting
* First start: the OS boots and the EC2 User Data script is run
* Following starts: The OS boots up
* Then your application starts, caches get warmed up, and all of that takes time.

## Hibernate
* The RAM state is preserved
* The instance boot is much faster than the above methods
* Under the hood, the RAM state is written to a file in EBS.
* The root EBS file must be encrypted (potential gotcha)
* Use cases:
    * Long running processing
    * Saving the RAM state
    * Services that take a long time to initialize

## More About Hibernate

* Many instance families supported
* Instance RAM size must be under 150GB
* Not supported for bare metal instances
* Works with many flavors of Linux + Windows
* Root Volume - must be EBS, encrypted, not instance store, and large
* Available for On-Demand, Reserved, and Spot instances
* An instance can not be hibernated for more than 60 days

## Enabling Hibernate

Hibernate is an option in the console under advanced options in a field called "Stop Hibernate Behavior." Just set to "Enable". 

In order to actually use hibernate, you have to make sure your EBS is configured correctly. Encrypt it and ensure it is large enough to contain the instance memory. I.E., if you use a T2Micro instance with 1GB of RAM, your EBS has to be encrypted and of at least 1GB in size. 

