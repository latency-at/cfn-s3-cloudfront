# CloudFormation Templates for S3+CloudFront stack

## Usage
Beside the stack-name, you need to specify:

- Domain: The domain name for the website
- ValidationDomain: The domain name to use for
  [certificate validation](http://docs.aws.amazon.com/acm/latest/APIReference/API_DomainValidationOption.html).

```
aws --region us-east-1 cloudformation create-stack \
  --stack-name YourStackName \
  --parameters ParameterKey=Domain,ParameterValue=www.example.com \
    ParameterKey=ValidationDomain,ParameterValue=example.com \
  --template-body "$(cat site.yml)"
```
