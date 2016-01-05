# Docker AWSCLI

[Docker](https://docker.io) image for running the [Amazon Web Services Command Line Interface](http://aws.amazon.com/cli/) based on [Alpine Linux](http://alpinelinux.org). Approximately 80mb.

## Usage

```sh
docker run jemmyw/awscli help
```

## AWS Credentials
There are two methods for setting up your AWS credentials:

1. Use environment variables. For example:

  ```sh
  docker run -t -e "AWS_ACCESS_KEY_ID=xxx" \
    -e "AWS_SECRET_ACCESS_KEY=xxx" \
    -e "AWS_DEFAULT_REGION=us-east-1" \
    jemmyw/awscli ec2 create-instance ...
  ```

2. Run from docker on an EC2 instance with an [IAM role](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/iam-roles-for-amazon-ec2.html).
