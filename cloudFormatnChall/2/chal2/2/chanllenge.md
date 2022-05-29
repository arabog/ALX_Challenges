ToDo
Write a CloudFormation script that:

1. Creates a VPC
It will accept the IP Range -also known as CIDR block- from an input parameter

2. Creates and attaches an Internet Gateway to the VPC

3. Creates Two Subnets within the VPC with Name Tags to call them “Public” 
and “Private”. These will also need input parameters for their ranges, just 
like the VPC.

4. The Subnet called “Public” needs to have a NAT Gateway deployed in it
This will require you to allocate an Elastic IP that you can then use to assign it to the NAT Gateway.

5. The Public Subnet needs to have the MapPublicIpOnLaunch property set 
to true. Use this reference for help.

6. The Private Subnet needs to have the MapPublicIpOnLaunch property set to false.

7. Both subnets need to be /24 in size. If you need assistance with IP math, 
you can use a subnet calculator such as this one.

8. You will need 2 Routing Tables, one named Public and the other one Private

9. Assign the Public and Private Subnets to their corresponding Routing table

10. Create a Route in the Public Route Table to send default traffic ( 0.0.0.0/0 ) to the Internet Gateway you created

11. Create a Route in the Private Route Table to send default traffic ( 0.0.0.0/0 ) to the NAT Gateway

12. Finally, once you execute this CloudFormation script, you should be able to delete it and create it again, over and over in a predictable and repeatable manner, this is the true verification of working Infrastructure-as-Code