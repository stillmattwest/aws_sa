# SSH Overview

SSH is the way to connect directly to Linux servers. 

You can use your terminal or a web browser called EC2 Instance Connect, but that only works with Amazon Linux v2.

## SSH With Linux or MacOS

There are three moving parts that make the connection work.
1. The correct terminal command
2. Your .pem file
3. A matching key on the EC2 instance (hence, a key pair)

The correct command for connecting to your EC2 instance via SSH is `ssh -i /path/to/your/.pem file ec-2user@xxx.xxx.xxx.xxx`

You can get your .pem file in the AWS console by going EC2 Dashboard => Network and Security (left-hand menu) => Key Pairs. You should see a key pair in there already. If you have the corresponding .pem file on your computer already, you should be set.

If you do NOT have the .pem file on your computer, that key pair is useless and you'll have to generate a new one. You can do this by right-clicking the existing key and selecting "Create Key Pair". That will give you a new .pem file, which you should store somewhere safe on your computer.

It does NOT create a corresponding key on the EC2 instance. 

You can manually add it. First, you have to create a new ssh key for the .pem on your own computer by entering the command: `ssh-keygen -y -f /path/to/your/.pem`

Then, copy the generated key.

Then connect to your instance via EC2-Connect, cd to ~/.ssh, and paste the new key to the end of the file. Save and exist and you should be able to ssh in from the local terminal.

The command to get verbose feedback for an ssh connection is ` ssh -i ~/path/to/your/.pem ec2-user@xxx.xxx.xxx.xxx -v`.


