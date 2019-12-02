# Single Instance running Webserver behind a classic ELB

Some basic CloudFormation to stand up an webserver on EC2 behind an ELB design to go into an AWS default VPC

## Delete Stack
`aws cloudformation delete-stack --stack-name single-instance  --region ap-southeast-1`

## Update Stack

`aws cloudformation update-stack --template-body file://templates/single_instance.yaml --stack-name single-instance --capabilities CAPABILITY_AUTO_EXPAND CAPABILITY_IAM --region ap-southeast-1`

## Create Stack

`aws cloudformation create-stack --template-body file://templates/single_instance.yaml --stack-name single-instance --capabilities CAPABILITY_AUTO_EXPAND CAPABILITY_IAM --region ap-southeast-1`

### Connecting to the host
`aws ssm start-session --target <instance-id> --region ap-southeast-1`
