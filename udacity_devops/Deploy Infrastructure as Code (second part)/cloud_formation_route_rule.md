```yaml


DefaultPublicRoute:
	Type: AWS::EC2::Route
	DependsOn: InternetGatewayAttachment
	Properties:
		RouteTableId: !Ref PublicRouteTable
		DestinationCidrBlock: 0.0.0.0/0
		GatewayId: !Ref InternetGateway


```


destination  0.0.0.0/0
go through the GatewayId
