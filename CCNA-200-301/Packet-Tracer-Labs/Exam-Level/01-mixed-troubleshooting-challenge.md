# Lab 01: Mixed Troubleshooting Challenge

## Objective

Practice diagnosing common CCNA-level faults in switching, routing, and IP addressing.

## Scenario

A small office network has lost partial connectivity after recent configuration changes. Your job is to identify and fix the issues.

## Topics

- VLAN assignment
- Trunk configuration
- Default gateway settings
- Interface status
- Static routing
- Basic device verification

## Challenge Rules

1. Build or load the topology.
2. Start a 30-minute timer.
3. Use only verification and configuration commands available in Cisco IOS.
4. Document every fault you find.
5. Confirm full connectivity before finishing.

## Troubleshooting Checklist

- Are all required interfaces up?
- Are PC IP addresses, masks, and gateways correct?
- Are access ports assigned to the right VLAN?
- Are trunks allowing the required VLANs?
- Are router interfaces or subinterfaces configured correctly?
- Are routes present in the routing table?

## Useful Commands

```text
show ip interface brief
show vlan brief
show interfaces trunk
show ip route
show running-config
ping
traceroute
```

## Notes

- Save the completed Packet Tracer file as `01-mixed-troubleshooting-challenge.pkt`.

