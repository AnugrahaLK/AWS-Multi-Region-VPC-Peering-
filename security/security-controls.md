# Security Controls

## Jump Server
TCP/22 from trusted administrator IP/CIDR.

## Private EC2
Allow only required administrative/application traffic from trusted internal sources.

## Cross-VPC Traffic
Allow only required protocols and ports between:
10.0.0.0/16 ↔ 192.0.0.0/16

Review Security Groups and Network ACLs when troubleshooting.
