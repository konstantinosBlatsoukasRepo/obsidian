some commands

```
aws --version
aws ec2 describe-instances

## start an instance
aws ec2 start-instances --instance-ids i-23451243fc23


## publish message from cli
aws sns publish --topic-arn arn:was:sns:.....  --message "my msg"


## s3 contents
aws s3 ls s3://codevr

aws iam list-users
aws configure set aws_session_token "" --profile default
aws configure set region us-east-1
aws configure list-profiles

## gitbash
setx AWS_ACCESS_KEY_ID AKIAIOSFODNN7EXAMPLE
setx AWS_SECRET_ACCESS_KEY wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
setx AWS_DEFAULT_REGION us-west-2


## create new profile
aws configure --profile TransetaAdmin


## create a bucketin us-east-1

aws s3api create-bucket --bucket my-033212455158-bucket --acl public-read-write --region us-east-1 --profile TransetaAdmin

## delete a bucket
aws s3api delete-bucket --bucket my-transeta8-bucket --profile TransetaAdmin
```