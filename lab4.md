# Custom VPC + EC2 Networking Lab
🎯 Objective - Build a VPC with a public subnet and launch an EC2 instance.

## Architecture
VPC
 ├── Public Subnet
 │    ├── Route Table → Internet Gateway
 │    └── EC2 Instance

### Steps

1. Create VPC (10.0.0.0/16)
2. Create Public Subnet
3. Create Internet Gateway + attach
4. Create Route Table (0.0.0.0/0 → IGW)
5. Launch EC2 in public subnet
6. SSH into EC2

### Validation

EC2 can access internet (ping google.com).

### Cleanup

Delete VPC + EC2.
