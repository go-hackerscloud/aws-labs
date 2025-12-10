# RDS MySQL Deployment Lab
🎯 Objective - Deploy RDS MySQL and access it using EC2.

## Architecture
EC2 → RDS MySQL

### Steps

1. Create RDS MySQL instance
2. Launch EC2 instance in same VPC
3. Install MySQL client
4. Connect:

mysql -h <RDS-ENDPOINT> -u admin -p

### Validation

Able to run SQL queries.

### Cleanup

Delete RDS + EC2.
