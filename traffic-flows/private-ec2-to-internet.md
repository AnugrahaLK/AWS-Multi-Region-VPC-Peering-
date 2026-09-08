# Private EC2 → Internet

```text
Private EC2
    ↓
Private Route Table
    ↓
0.0.0.0/0
    ↓
NAT Gateway
    ↓
Internet Gateway
    ↓
Internet
```

The NAT Gateway performs source address translation for outbound Internet connectivity. The private EC2 remains without a public IP.
