```yml
WebAppGroup:
    Type: AWS::AutoScaling::AutoScalingGroup
    Properties:
      VPCZoneIdentifier:
      - Fn::ImportValue: 
          !Sub "${EnvironmentName}-PRIV-NETS"
      LaunchConfigurationName:
        Ref: WebAppLaunchConfig
      MinSize: '3'
      MaxSize: '5'
      TargetGroupARNs:
      - Ref: WebAppTargetGroup
      HealthCheckGracePeriod: 60
      HealthCheckType: ELB
```