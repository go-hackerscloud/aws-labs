# S3 → Lambda → DynamoDB ETL Pipeline Lab
🎯 Objective

Simulate a small ETL process where S3 triggers Lambda to update DynamoDB.

## Architecture
S3 (Trigger) → Lambda → DynamoDB

### Steps

1. Create DynamoDB table Users with userId as primary key
2. Create Lambda function:

import json
import boto3

dynamo = boto3.resource('dynamodb')
table = dynamo.Table('Users')

def lambda_handler(event, context):
    for record in event['Records']:
        data = json.loads(record['body'])
        table.put_item(Item=data)
    return 'Success'


3. Create S3 bucket
4. Configure S3 → Lambda event trigger (PUT)
5. Upload sample JSON file:

{"userId": "101", "name": "Rohit", "role": "Cybersecurity"}

### Validation

Record appears in DynamoDB table.

### Cleanup

Delete DynamoDB, S3, Lambda.
