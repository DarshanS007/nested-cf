# nested-cf
Nested AWS CloudFormation Stack for ASG,ALB and VPC


This is a Nested stack having two stacks  Parent and child stack ,where the parent stack is the main stack where the parameter and mappings  are configured to create the resources ASG and ALB , Child stack created here is used to create the vpc 





Parent stack consists of the following resources 

1) Auto Scaling Group :- which includes Launch template, Auto scaling policy, Target Tracking policy,Instance security group and Key pair
2) Application Load Balancer:- which inculdes Target Group,Application Load Balancer and ALB Security Group


Child stack consists of the following resource

1) VPC :- which includes     VPC with CIDR ,3 Public Subnets ,3 Private Subnets ,Internet Gateway 3 NAT Gateways (one in each public subnet)and public and Private Route Table
