# Lab 04: IP Addressing Practice

## Objective

Practice assigning correct IPv4 addresses, subnet masks, and default gateways.

## Topology

- 1 router
- 2 switches
- 4 PCs

## Addressing Plan

| Network | Purpose | Gateway |
| --- | --- | --- |
| 192.168.1.0/24 | LAN 1 | 192.168.1.1 |
| 192.168.2.0/24 | LAN 2 | 192.168.2.1 |

## Tasks

1. Build two LANs connected through one router.
2. Configure router interfaces for both LANs.
3. Assign static IP settings to all PCs.
4. Verify that PCs can ping their default gateway.
5. Verify that PCs can ping across LANs.

## Verification

```text
show ip interface brief
ping
traceroute
```

## Notes

- Save the completed Packet Tracer file as `04-ip-addressing-practice.pkt`.

