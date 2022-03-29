
```
aws cloudformation create-stack  --stack-name challenge1 --region us-east-1 --template-body file://challenge1.yml
```

glossary:

-   **Name**: A name you want to give to the resource (does this have to be unique across all resource types?)  
-   **Type**: Specifies the actual hardware resource that you’re deploying.  
-   **Properties**: Specifies configuration options for your resource. Think of these as all the drop-down menus and checkbox options that you would see in the AWS console if you were to request the resource manually.  
-   **Stack**: A stack is a group of resources. These are the resources that you want to deploy, and that are specified in the YAML file.

Example:

```yml
Parameters:
	EnvironmentName:
		Description: An environment name
		Type: String
	VpcCIDR:
		Description: Ip range
		Type: String
		Default: 10.0.0.0/16
Resources:
	VPC:
		Type: AWS::EC2::VPC
		Properties:
			CidrBlock: !Ref VpcCIDR
			EnableDnsHostnames: true
			Tags:
				- Key: Name
				  Value: !Ref EnvironmentName
```