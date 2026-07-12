# Lab 01: VLANs and Trunking

## Objective

Create VLANs on switches, assign access ports, configure a trunk link, and verify same-VLAN connectivity across switches.

## Topology

- 2 switches
- 4 PCs
- One trunk link between switches

## VLAN Table

| VLAN | Name | Subnet |
| --- | --- | --- |
| 10 | SALES | 192.168.10.0/24 |
| 20 | IT | 192.168.20.0/24 |

## Tasks

1. Create VLAN 10 and VLAN 20 on both switches.
2. Assign two PCs to VLAN 10 and two PCs to VLAN 20.
3. Configure the inter-switch link as a trunk.
4. Configure static IP addresses on all PCs.
5. Verify that PCs in the same VLAN can communicate.
6. Verify that PCs in different VLANs cannot communicate without routing.

## Useful Commands

```text
show vlan brief
show interfaces trunk
show running-config
```

## Notes

- Save the completed Packet Tracer file as `01-vlan-and-trunking.pkt`.

