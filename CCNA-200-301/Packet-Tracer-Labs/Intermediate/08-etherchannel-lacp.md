# Lab 08: EtherChannel with LACP

## Objective

Bundle multiple switch links into one logical EtherChannel using LACP.

## Topology

- 2 switches
- 2 or 4 links between switches
- 2 PCs

## Tasks

1. Connect multiple links between switches.
2. Configure the links as trunks.
3. Configure LACP EtherChannel.
4. Verify the Port-channel interface.
5. Test connectivity across the switches.

## Example Commands

```text
interface range f0/1-2
switchport mode trunk
channel-group 1 mode active

interface port-channel 1
switchport mode trunk
```

## Verification

```text
show etherchannel summary
show interfaces port-channel 1
show interfaces trunk
```

## Notes

- Save the completed Packet Tracer file as `08-etherchannel-lacp.pkt`.

