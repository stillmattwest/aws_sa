# EC2 Basics

EC2 is one of the most popular AWS offerings. It stands for **Elastic Compute Cloud**.

EC2 Consists of the Following:
* Renting virtual machines (EC2)
* Storing data on virtual drives (EBS)
* Distributing load across machines (ELB)
* Scaling the services using auto-scaling groups (ASG)

Knowing how EC2 works is fundamental to understanding the cloud.

## EC2 Sizing and Configuration Options

We can configure the following:

* OS (Linux, Windows, MacOS all available)
* Compute Power and Cores (CPU)
* RAM
* Storage Space
    * Network-Attached Storage (EBS and EFS)
    * Hardware Storage (EC2 Instance Store)
* Network Card (Speed, Public IP)
* Firewall Rules (Security Group)
* Bootstrap Script (Configures the machine at first launch. EC2 User Data)

There are more configuration options than this, but these are important for the ASAA cert

## EC2 User Data

EC2 User Data allows us to bootstrap our instances using a script.

Bootstrapping means launching commands when the machine starts

The script is only run once at the first start of the instance.

EC2 user data is used to automate boot tasks such as:

* Installing updates
* Installing software
* Downloading common files from the Internet
* Anything else we might want to do

## EC2 Instance Types

The instance type is how much machine we want. There are hundreds of types, ranging from tiny machines like the t2.micro with only 1GB of RAM and crappy network performance to huge machines like the m5.2xlarge with 128GB of RAM and 10Gbs network. Other types might not be quite so huge but will have attached SSDs or other options. 

Pricing of course depends on use. It would be possible to do something like spinning up a powerful development machine for less than 2 bucks per hour and shutting it off when it wasn't needed. For example, a C3.8xlarge with 16 cores (32 threads) 10 Gbs networking and 640GB of SSD would cost about 6.72 per day if you were on it four hours per day. It adds up, though. That's about 144 per month. 

That's a huge machine, though. A more reasonable option might be the c3.xlarge. That's a 2 core, 4 thread machine with 7.5GB of RAM and 80GB of SSD. That only runs 0.37 per hour, or 1.48 per day. 31 per month. 

Now... there's basically no point in doing any of that since physical computers are so cheap, but you *could* do it. 

## Launching Instances

It is very easy to launch a new AWS instance of whatever type and this can be done from the console or CLI. 

One thing to keep in mind if you're going to start and stop and instance frequently is that you will get a new public IP every time you start (makes sense). 



