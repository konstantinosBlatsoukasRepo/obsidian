```yaml
NatGateWay2:
	Type: AWS::EC2::NatGateway
	Properties:
		AllocationId: !GetAtt NatGateway2EIP.AllocationId
		SubnetId: !Ref PublicSubnet2
```