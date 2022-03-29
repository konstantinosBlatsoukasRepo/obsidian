```
PublicSubnet1:
	Type: AWS::EC2::Subnet
	Properties:
		VpcId: !Ref VPC
		AvailabilityZone: !Select [ 1, !GetAZs, '' ]
		CidrBlock: !Ref PrivateSubnet2CIDR
		MapPublicIpOnLaunch: false
		Tags: 
			- Key: Name
			  Vaie: !Sub ${Environment} Private Subnet (AZ2)
```