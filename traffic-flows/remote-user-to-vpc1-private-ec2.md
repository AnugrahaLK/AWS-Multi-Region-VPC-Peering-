# Remote User → VPC 1 Private EC2

```text
Remote User → Internet → IGW → Public Route Table → Jump Server
Jump Server → Private Route Table → Private EC2
```

First TCP connection:
```text
Source = Remote User Public IP
Destination = Jump Server Public IP
Protocol = TCP
Destination Port = 22
```

Second TCP connection:
```text
Source = Jump Server Private IP
Destination = Private EC2 Private IP
Protocol = TCP
Destination Port = 22
```

The private EC2 does not need a public IP.
