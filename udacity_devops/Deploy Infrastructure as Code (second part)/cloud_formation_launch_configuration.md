specification (how much memory, how musch space etc)
of a AWS EC2 instances 
+ You can attach a Security Group ++
+ IamgeId: AMI (Amazon machine image), OS etc.


```yml
Resources:
  WebAppLaunchConfig:
    Type: AWS::AutoScaling::LaunchConfiguration
    Properties:
      UserData:
        Fn::Base64: !Sub |
          #!/bin/bash
          apt-get update -y
          apt-get install apache2 -y
          systemctl start apache2.service
          cd /var/www/html
          echo "Udacity Demo Web Server Up and Running!" > index.html
      ImageId: ami-0ac73f33a1888c64a
      KeyName: VocareumKey2
      SecurityGroups:
      - Ref: WebServerSecGroup
      InstanceType: t3.small
      BlockDeviceMappings:
      - DeviceName: "/dev/sdk"
        Ebs:
          VolumeSize: '10'

```