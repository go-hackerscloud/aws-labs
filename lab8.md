# Load Balancer + Auto Scaling Lab
🎯 Objective - Simulate high availability setup using ALB + ASG.

## Architecture
ALB → Auto Scaling Group → EC2 Instances

### Steps

1. Create Launch Template
2. Add User Data script (web server)
3. Create Auto Scaling Group
4. Create Application Load Balancer
5. Test DNS name of ALB

### Validation

Requests hit multiple backend EC2 instances.

### Cleanup

Delete ASG + ALB + Launch Template.
