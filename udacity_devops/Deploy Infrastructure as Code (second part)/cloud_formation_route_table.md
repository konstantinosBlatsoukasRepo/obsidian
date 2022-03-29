PublicRouteTable:
	Type: AWS::EC2::RouteTable
	Properties:
		VpcId: !Ref VPC
		Tags:
			- Key: Name
			Value: !Sub ${EnvironmentName} Public Routes