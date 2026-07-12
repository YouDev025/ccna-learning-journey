# Lab 02: Small Enterprise Build

## Objective

Build a small enterprise network from requirements and verify complete connectivity.

## Requirements

- At least 2 switches
- At least 1 router
- VLAN 10 for users
- VLAN 20 for IT
- VLAN 99 for management
- Inter-VLAN routing
- Static addressing for infrastructure devices
- DHCP for user PCs

## Suggested Addressing

| Network | Purpose |
| --- | --- |
| 192.168.10.0/24 | Users |
| 192.168.20.0/24 | IT |
| 192.168.99.0/24 | Management |

## Tasks

1. Design and build the topology.
2. Configure VLANs and trunks.
3. Configure inter-VLAN routing.
4. Configure DHCP pools.
5. Configure switch management IP addresses.
6. Verify that end devices receive addresses.
7. Verify connectivity between VLANs.
8. Save device configurations.

## Verification

```text
show vlan brief
show interfaces trunk
show ip interface brief
show ip dhcp binding
show ip route
ping
```

## Notes

- Save the completed Packet Tracer file as `02-small-enterprise-build.pkt`.

