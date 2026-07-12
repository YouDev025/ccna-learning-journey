# Lab 14: Subnetting Small LANs

## Objective

Practice subnetting one network into smaller LANs and assigning addresses.

## Scenario

You are given the network `192.168.10.0/24`. Create four smaller LANs.

## Topology

- 1 router
- 4 switches
- 4 PCs

## Tasks

1. Subnet `192.168.10.0/24` into four equal subnets.
2. Assign one subnet to each LAN.
3. Configure router interfaces or subinterfaces.
4. Configure each PC with an IP address, subnet mask, and default gateway.
5. Verify connectivity to each default gateway.

## Suggested Subnets

| LAN | Network |
| --- | --- |
| LAN 1 | 192.168.10.0/26 |
| LAN 2 | 192.168.10.64/26 |
| LAN 3 | 192.168.10.128/26 |
| LAN 4 | 192.168.10.192/26 |

## Verification

```text
show ip interface brief
ping
```

## Notes

- Save the completed Packet Tracer file as `14-subnetting-small-lans.pkt`.

