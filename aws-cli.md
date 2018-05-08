## AWS-CLI


### What

Run AWS-CLI on your local laptop using a Docker Image

### Why

Easy

### How

*Prerequisites*
```
dnf install docker
mkdir -m 0777 $HOME/.aws
```
*Run*
```
alias aws="docker run -t --rm -v $HOME/.aws:/root/.aws blendle/aws-cli"
aws configure
```

*Result*
```
cat ~/.aws/config
[default]
region=eu-west-1
output=json

 cat ~/.aws/credentials
[default]
aws_access_key_id=...
aws_secret_access_key=...
```
