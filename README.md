# AWS-CloudFormation-Templates
Some CloudFormation templates for reference

## RestApi_with_Lambda_and_CodeBuild_template.yaml
Creates a custom subdomain that is connected to API Gateway serving as a proxy for a Lambda Function. The Lambda Function is CICD ready with CodeBuild. This will be referred futher as the "Microservice template".

#### Resources Created:
- LambdaFunction (AWS::Lambda::Function)
- APIGatewayRestAPI (AWS::ApiGateway::RestApi)
- APIGatewayResource (AWS::ApiGateway::Resource)
- APIGatewayMethod (AWS::ApiGateway::Method)
- APIGatewayDeployment (AWS::ApiGateway::Deployment)
- APIGatewayPermission (AWS::Lambda::Permission)
- LambdaIAMRole (AWS::IAM::Role)
- CodeBuildIAMRole (AWS::IAM::Role)
- LambdaCWLogGroup (AWS::Logs::LogGroup)
- CodeBuildProject (AWS::CodeBuild::Project)
- CustomDomain (AWS::ApiGateway::DomainName)
- RecordSet (AWS::Route53::RecordSet)
- APIMapping (AWS::ApiGateway::BasePathMapping)

## MultiMicroserviceDeployment_template.yaml
Creates multiple Microservices as nested stacks
#### Resources Created:
- Microservice1 (AWS::CloudFormation::Stack)


# References:
- [AWS Docs](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/)
- ["Configure a Custom Domain for AWS API Gateway" by Jens Eickmeyer](https://scratchpad.blog/serverless/howto/configure-a-custom-domain-for-aws-api-gateway/)
- ["How to setup API Gateway Custom Domain using CloudFormation" by Preeti](https://cloudkatha.com/api-gateway-custom-domain-using-cloudformation/)
