# Lab 04: OSPF Troubleshooting

## Objective

Diagnose and fix OSPF neighbor and route advertisement problems.

## Topics

- OSPF area mismatch
- Passive interfaces
- Incorrect wildcard masks
- Network type and hello/dead timers
- Missing route advertisements

## Tasks

1. Build a three-router OSPF topology.
2. Intentionally introduce at least three OSPF faults.
3. Use show commands to identify each issue.
4. Restore OSPF adjacencies.
5. Verify all LAN routes are learned through OSPF.

## Verification

```text
show ip ospf neighbor
show ip ospf interface brief
show ip protocols
show ip route ospf
ping
```

## Notes

- Save the completed Packet Tracer file as `04-ospf-troubleshooting.pkt`.

