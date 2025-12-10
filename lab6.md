# CloudWatch Monitoring & Alerts Lab
🎯 Objective - Trigger an alert when EC2 CPU usage exceeds 70%.

## Architecture
EC2 → CloudWatch Alarm → SNS Email

### Steps

1. Launch EC2
2. Create SNS topic → subscribe with email
3. Create CloudWatch CPU Alarm
4. Install CPU stress tool:

sudo amazon-linux-extras install epel -y
sudo yum install stress -y
stress --cpu 80

5. Wait for alarm

### Validation

Email alert received.

### Cleanup

Delete alarm + SNS + EC2.
