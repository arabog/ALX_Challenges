Research the EC2 Parameter Store
One way to avoid hard-coding ever-changing values into your server infrastructure is by using parameters. Examples of parameters that frequently change include database connection details, and sensitive data, such as passwords and secret API access keys.

Using the AWS CLI Tool, store and retrieve parameters from the EC2 Parameter Store. Play around with changing the value from the EC2 Console and not just the CLI Tool.

It’s critical that you practice this, as this is not only a best practice but also a common practice.

DON'T OPEN
https://github.com/udacity/nd9991-c2-Infrastructure-as-Code-v1-Exercises_Solution


Soln:
-------------------------
This is how you store a value in the Parameter Store:

aws ssm put-parameter --name "DBURL" --value "testdb.com" --type String --overwrite

In this case, storing the parameter DBURL with the value testdb.com
and overwriting if the parameter already exists.
-------------------------

This is how you get a parameter from the Parameter Store:

aws ssm get-parameter --name "DBURL"

The output will be in JSON format,so, 
you'll need to parse the "Value" from it.
-------------------------

In order to do this from your EC2 Instances, you'll need a role
assigned that provides access to Systems Manager (SSM)


Parameter Store
In the EC2 console, find the parameter store and add few parameters

Use d CLI to retrieve your parameters

Try updating ur paramters from d command line and also creating new ones