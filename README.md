# CloudFormation Examples

This repository contains AWS CloudFormation templates for deploying common AWS resources.

## Templates

- **s3.yaml**: Creates an S3 bucket with a customizable name and tags.
- **ec2.yaml**: Creates an EC2 instance with an associated security group that allows SSH access.

## Usage

1. Ensure you have AWS CLI configured with appropriate permissions.
2. Deploy the templates using the CloudFormation console or AWS CLI:

   ```bash
   aws cloudformation create-stack --stack-name my-stack --template-body file://template.yaml
   ```

Replace `template.yaml` with the desired template file (e.g., `s3.yaml` or `ec2.yaml`).

## Parameters

- For `s3.yaml`:
  - `s3BucketName`: Name of the S3 bucket (default: cloudformation-s3-bucket-prajwal)

- For `ec2.yaml`:
  - `InstanceName`: Name of the EC2 instance (default: MyEC2Instance)
  - `InstanceType`: EC2 instance type (default: t3.micro)
  - `KeyName`: Existing EC2 KeyPair name (default: devops-intern)
  - `ImageId`: AMI ID (default: ami-02d26659fd82cf299)

## Outputs

- `s3.yaml`:
  - `Arn`: ARN of the created S3 bucket
  - `WebsiteURL`: Website URL of the S3 bucket

- `ec2.yaml`:
  - `InstanceId`: ID of the created EC2 instance
  - `PublicIP`: Public IP address of the EC2 instance

## Contributing

Feel free to contribute additional templates or improvements.