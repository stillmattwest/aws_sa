# Security Groups and Classic Ports

Security Groups are fundamental to AWS security.


Security groups only contain ALLOW rules.

Security groups rules can reference by IP or Security Group.

Again, security groups only contain allow rules. Otherwise, they are much like firewalls.

Security Groups Regulate:

* Access to Ports

* Authorized IP ranges (IPv4 and IPv6)

* Control of inbound traffic

* Control of outbound traffic

By default, all outbound traffic is allowed and all inbound traffic is dropped. 

## Security Group Basics

* Security Groups can be attached to multiple instances

* Security Groups are bound to a region + VPC combination. If you switch either regions or VPCs, you have to create new security groups. 

Pro Tip: Create a security group just for SSH access. 

Time outs are likely a symptom of a security group problem.

Other application errors mean traffic is being allowed through.

It is possible to attach security group rules to other security groups. IE, all the devices in a given security group are allowed through on the specified ports.

## Classic Ports

<table>
<tr>
<th>PORT</th>
<th>SERVICE</th>
<th>DESCRIPTION</th>
<tr>
  <td>22</td>
  <td>SSH or SFTP</td>
  <td>Secure file transfer and login</td>
</tr>
<tr>
  <td>21</td>
  <td>FTP</td>
  <td>File Transfer Protocol</td>
</tr>
<tr>
  <td>80</td>
  <td>HTTP</td>
  <td>HyperText Transfer Protocol</td>
</tr>
<tr>
  <td>443</td>
  <td>HTTPS</td>
  <td>Secure HTTP</td>
</tr>
<tr>
  <td>3389</td>
  <td>RDP</td>
  <td>Remote Desktop Protocol</td>
</tr>

</table>




