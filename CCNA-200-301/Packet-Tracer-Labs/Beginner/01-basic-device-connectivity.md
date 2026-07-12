# Lab 01: Basic Device Connectivity

## Objective

Build a simple LAN and verify end-to-end connectivity between two PCs through a switch.

## Topology

- 2 PCs
- 1 switch
- Copper straight-through cables

## Addressing Table

| Device | Interface | IP Address | Subnet Mask |
| --- | --- | --- | --- |
| PC1 | FastEthernet0 | 192.168.1.10 | 255.255.255.0 |
| PC2 | FastEthernet0 | 192.168.1.20 | 255.255.255.0 |

## Tasks

1. Add two PCs and one switch.
2. Connect both PCs to the switch.
3. Configure static IP addresses on both PCs.
4. Test connectivity from PC1 to PC2.

## Verification

From PC1:

```text
ping 192.168.1.20
```

Expected result: successful replies.

## Notes

- Save the completed Packet Tracer file as `01-basic-device-connectivity.pkt`.

