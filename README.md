# Runway CICD

## Using this module you can create the following

1. Create a runway project to deploy 2 CloudFormation templates that create the following resources:

● VPC CFN ○ Resources

■ VPC.

■ 2 public subnets in 2 different Availability Zones.

■ 2 private subnets in 2 different Availability Zones.

■ Internet Gateway.

■ Route Tables and Routes.

■ Network Access Control List.

○

■ NAT Gateway. Parameters

■ VPC CIDR.

■ Subnets CIDRs.

● Servers CFN ○

○

Resources:

■ Bastion host.

■ Web instance in every subnet.

■ Bastion security group (allow ssh from specific IP).

■ Public Instance security group (allow 80 from everywhere, 22 from VPC CIDR).

■ Private Instance security group (allow 80, 22 from VPC CIDR). Parameters:

■ Key name.

■ Bastion allowed IP.

■ Instances types.


2. Install Jenkins server and runway on EC2 instance manually. 

3. Create a Project in Jenkins to execute the runway build command.

4. Use Jenkins git webhook to trigger the builds when a pull request is merged to master.
