# IAM Role + EC2 → S3 Access Lab
🎯 Objective - Enable EC2 to access S3 buckets using IAM roles (no access keys).

## Architecture
EC2 Instance → IAM Role → S3

### Steps

1. Create IAM Role → Attach AmazonS3ReadOnlyAccess
2. Attach role to EC2 instance
3. SSH into EC2
4. Run:
aws s3 ls

### Validation

EC2 lists S3 buckets successfully.

### Cleanup

Remove IAM role.
