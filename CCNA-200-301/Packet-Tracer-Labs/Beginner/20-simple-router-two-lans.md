# Lab 20: Simple Router with Two LANs

## Objective

Connect two separate LANs using one router.

## Topology

- 1 router
- 2 switches
- 4 PCs

## Addressing Plan

| LAN | Network | Gateway |
| --- | --- | --- |
| LAN A | 192.168.11.0/24 | 192.168.11.1 |
| LAN B | 192.168.12.0/24 | 192.168.12.1 |

## Tasks

1. Build the topology.
2. Configure both router interfaces.
3. Configure static IP settings on all PCs.
4. Ping from each PC to its default gateway.
5. Ping from LAN A to LAN B.

## Verification

```text
show ip interface brief
ping
traceroute
```

## Notes

- Save the completed Packet Tracer file as `20-simple-router-two-lans.pkt`.

