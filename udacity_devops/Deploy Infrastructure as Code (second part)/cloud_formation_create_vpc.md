```yml
Parameters:
	 EnvironmentName:
	 Description: An environment name
	 Type: String
VpcCIDR:
	 Description: IP range
	 Type: String
	 Default: 10.0.0.0/16

  

Resources:

# creates a virtual private cloud (e.g. includes all the resources for the physical infrastrucutre)

 VPC:
	 Type: AWS::EC2::VPC
	 Properties:
		 CidrBlock: !Ref VpcCIDR
		 EnableDnsHostnames: true
	 Tags:
		 - Key: Name
		 Value: !Ref EnvironmentName

# internet gateway (software component) allows the vpc to communicate to the internet
# not a psysical device
# performs a NAT (network address transaltion)
# Horizontally scaled, redntabt and high available
```