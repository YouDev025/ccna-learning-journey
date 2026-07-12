# Lab 02: Router-on-a-Stick

## Objective

Configure inter-VLAN routing using router subinterfaces and an 802.1Q trunk.

## Topology

- 1 router
- 1 switch
- 4 PCs

## VLAN Table

| VLAN | Name | Gateway |
| --- | --- | --- |
| 10 | SALES | 192.168.10.1 |
| 20 | IT | 192.168.20.1 |

## Tasks

1. Create VLANs on the switch.
2. Assign PC access ports to the correct VLANs.
3. Configure the switch port connected to the router as a trunk.
4. Configure router subinterfaces for VLAN 10 and VLAN 20.
5. Configure PC IP addresses and default gateways.
6. Verify inter-VLAN connectivity.

## Router Example

```text
interface g0/0.10
encapsulation dot1Q 10
ip address 192.168.10.1 255.255.255.0

interface g0/0.20
encapsulation dot1Q 20
ip address 192.168.20.1 255.255.255.0

interface g0/0
no shutdown
```

## Verification

```text
show ip interface brief
show interfaces trunk
ping
```

## Notes

- Save the completed Packet Tracer file as `02-router-on-a-stick.pkt`.

