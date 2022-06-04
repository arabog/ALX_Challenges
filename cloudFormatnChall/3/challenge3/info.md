https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_EC2.html

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_IAM.html

https://docs.aws.amazon.com/cli/latest/reference/cloudformation/deploy/index.html


aws cloudformation create-stack --stack-name $1 --template-body file://$2  --parameters file://$3 --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-west-2

If you are running the script using the CLI and the cloudformation create-stack command, please remember to include the --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" option (see the AWS CLI Documentation). This is because we are creating an IAM Role to provide permissions and we want to make the person executing create-stack aware of this fact.


Scalable Microservices with Kubernetes:
https://www.udacity.com/course/scalable-microservices-with-kubernetes--ud615


Cloudformation Validator
https://www.cloudformation-validator.com/