# Lab 05: Switching Troubleshooting

## Objective

Troubleshoot a switched network with VLAN, trunk, STP, and EtherChannel issues.

## Topics

- VLAN creation
- Access port assignment
- Trunk native VLAN
- Allowed VLAN lists
- STP blocked ports
- EtherChannel mismatch

## Tasks

1. Build a three-switch topology.
2. Configure multiple VLANs.
3. Introduce switching faults.
4. Troubleshoot same-VLAN and inter-switch connectivity.
5. Document the command that revealed each fault.
6. Fix the configuration and retest.

## Verification

```text
show vlan brief
show interfaces trunk
show spanning-tree
show etherchannel summary
ping
```

## Notes

- Save the completed Packet Tracer file as `05-switching-troubleshooting.pkt`.

