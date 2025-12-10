# Lambda + API Gateway Serverless API Lab
Objective - Create a simple serverless REST API.

## Architecture
Client → API Gateway → Lambda → Response

### Steps

1. Create Lambda function using Python:

def lambda_handler(event, context):
    return {
        'statusCode': 200,
        'body': 'Hello from AWS Lambda!'
    }


2. Create API Gateway → REST API
3. Add GET /hello route
4. Integrate Lambda
5. Deploy API
6. Test endpoint URL

### Validation

Endpoint returns "Hello from AWS Lambda!".

### Cleanup

Delete API Gateway + Lambda.
