```yml
 InternetGateway:
	 Type: AWS::EC2::InternetGateway
	 Properties:
		 - Key: Name
		Value: !Ref EnvironmentName
 InternetGatewayAttachment:
	 Type: AWS::EC2::VPCGatewayAttachment
	 Properties:
		 InternetGatewayId: !Ref InternetGateway
		 VpcId: !Ref VPC
 ```