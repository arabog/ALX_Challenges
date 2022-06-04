In this exercise, you have been tasked with deploying a Linux server in a private subnet, using the infrastructure that you created in a previous exercise. In the future, this machine will be a web server that sits behind a load balancer, so it never needs to be public, as long as the Load Balancer can reach it.

ToDo
Use the infrastructure we created earlier to build and deploy the following:

EC2 Instance: An Amazon Linux 2 EC2 server in the private subnet. Choose the right AMI ID as applicable to your region and the t3.micro instance-type.

SecurityGroup: A security group for the server, that allows inbound port 80 access, for future use.

IAM Role and InstanceProfile: The IAM Role to allow EC2 Session Manager to access our server. An InstanceProfile will allow passing the IAM role to our server.

You will provide input parameters to this script, for future expansion and flexibility.

Bonus/Optional: Instead of hard-coding the VPC and Subnet ID, use the import-export feature to cross reference the resources created in Challenge 2.

https://video.udacity-data.com/topher/2021/February/602bdbbe_challenge3/challenge3.yml