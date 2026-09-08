# Packet-Level Traffic Flow

## VPC 1 → VPC 2

```text
Source      = 10.0.135.27
Destination = 192.0.11.187
Protocol    = ICMP
```

The destination belongs to `192.0.0.0/16`.

Route:
```text
192.0.0.0/16 → VPC Peering
```

Therefore the packet is sent through VPC Peering.

## Private EC2 → Internet

For an Internet destination:
```text
0.0.0.0/0 → NAT Gateway
```

The NAT Gateway provides outbound Internet connectivity through the Internet Gateway.

## Route Selection

AWS uses the most specific matching route:
```text
192.0.0.0/16 → VPC Peering
0.0.0.0/0    → NAT Gateway
```

Traffic destined for `192.0.x.x` uses the peering route rather than the default NAT route.
