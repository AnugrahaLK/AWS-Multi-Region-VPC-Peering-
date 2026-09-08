# Connectivity Testing & Troubleshooting

```bash
ip addr
ip route
ping <destination-private-ip>
ssh -v user@<private-ip>
nc -zv <destination-ip> 22
traceroute <destination-ip>
```

Traceroute may show missing intermediate hops in AWS because infrastructure may not respond to TTL-expired probes.

Troubleshooting order:
EC2 / ENI → Security Group → Network ACL → Route Table → VPC Peering → Destination Route Table → Destination Security Group → Destination Network ACL

Check both forward and return routes.
