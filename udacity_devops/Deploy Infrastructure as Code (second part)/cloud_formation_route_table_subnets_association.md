```yaml

Type: AWS::EC2::SubnetRouteTableAssociation
Properties:
	RouteTableId: !Ref PublicRouteTable
	SubnetId: !Ref PublicSubnet2

```