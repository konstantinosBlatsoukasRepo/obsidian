```yaml
NatGateway1EIP:
	Type: AWS::EC2::EIP
	DependsOn: InternetGatewayAttachment
	Properties:
		Domain: vpc
```