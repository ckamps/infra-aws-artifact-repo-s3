# AWS Cloud Foundation S3 Artifact Repository CloudFormation Template

Creates an S3 bucket to house cloud foundation artifacts such as CloudFormation templates, IAM SAML provider metadata files, etc. and grants administrators in member accounts access to objects in the bucket.

This CloudFormation template is a Jinja2 template file that must first be processed to render a usable CloudFormation template.

## Usage

The rendered form of this template is expected to be applied to the admin account.  See ... for details on how this template is intended to be used.

### Parameters

|Parameter|Required|Description|Default|
|---------|--------|-----------|-------|
|`pOrg`|Optional|Organizational qualifier used a prefix for S3 bucket.|`acme`|
|`pBaseBucketName`|Optional|Base name of the S3 bucket. Will be qualified with the prefix of `${pOrg}` and a suffix of `-${AWS::AccountId}-${AWS::Region}`|`infra-artifacts`|
