# CloudFormation Beginner Lab
🎯 Objective - Deploy EC2 + Security Group using a CloudFormation template.

## Architecture
CloudFormation → EC2 + SG

### Steps

1. Create stack using YAML:

Resources:
  MyEC2:
    Type: AWS::EC2::Instance
    Properties:
      InstanceType: t2.micro
      ImageId: ami-0c02fb55956c7d316
      SecurityGroupIds:
        - !Ref WebSG

  WebSG:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: Allow HTTP
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: 80
          ToPort: 80
          CidrIp: 0.0.0.0/0


2. Deploy stack
3. Validate resources
4. Delete stack

### Validation

EC2 is created without manual steps.

### Cleanup

Delete CloudFormation stack.
