# Remote User → VPC 2 Private EC2

```text
Remote User → Internet → IGW → VPC 2 Jump Server
VPC 2 Jump Server → Private IP → VPC 2 Private EC2
```

The public connection terminates at the Jump Server. A separate internal SSH connection is then established to the private EC2.
