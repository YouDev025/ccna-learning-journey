# Lab 11: Port Security Introduction

## Objective

Configure basic switch port security to limit which device can connect to an access port.

## Topology

- 1 switch
- 2 PCs

## Tasks

1. Connect PC1 to an access port.
2. Configure the port as an access port.
3. Enable port security.
4. Limit the port to one MAC address.
5. Use sticky MAC learning.
6. Move PC2 to the secured port and observe the result.

## Example Commands

```text
interface f0/1
switchport mode access
switchport port-security
switchport port-security maximum 1
switchport port-security mac-address sticky
switchport port-security violation shutdown
```

## Verification

```text
show port-security
show port-security interface f0/1
show running-config
```

## Notes

- Save the completed Packet Tracer file as `11-port-security-introduction.pkt`.

