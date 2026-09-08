# VPC 1 Private EC2 → VPC 2 Private EC2

Example:
```text
VPC 1 EC2 = 10.0.135.27
VPC 2 EC2 = 192.0.11.187
```

Packet:
```text
Source      = 10.0.135.27
Destination = 192.0.11.187
Protocol    = ICMP
```

Route:
```text
192.0.0.0/16 → VPC Peering
```

Flow:
```text
VPC 1 Private EC2
        ↓
VPC 1 Private Route Table
        ↓
VPC Peering
        ↓
VPC 2 Route Table
        ↓
VPC 2 Private EC2
```

Return path:
```text
10.0.0.0/16 → VPC Peering
```

No NAT Gateway is required for this private VPC-to-VPC path.
