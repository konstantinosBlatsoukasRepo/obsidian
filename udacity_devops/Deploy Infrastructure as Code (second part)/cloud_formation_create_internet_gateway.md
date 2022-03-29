```yml
 Parameters:
	 EnvironmentName:
		 Description: An environment name
		 Type: String

 InternetGateway:
	 Type: AWS::EC2::InternetGateway
	 Properties:
		 - Key: Name
		Value: !Ref EnvironmentName

 ```