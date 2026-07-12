# Lab 18: Duplex and Speed Settings

## Objective

View and configure interface speed and duplex settings.

## Topology

- 1 switch
- 2 PCs

## Tasks

1. Connect both PCs to the switch.
2. Check the status of the connected switch ports.
3. Configure speed and duplex manually on one switch port.
4. Return the port to automatic negotiation.
5. Compare interface output before and after the changes.

## Useful Commands

```text
show interfaces status
show interfaces f0/1
interface f0/1
speed 100
duplex full
speed auto
duplex auto
```

## Questions

- What does full duplex mean?
- Why can duplex mismatch cause performance issues?

## Notes

- Save the completed Packet Tracer file as `18-duplex-and-speed-settings.pkt`.

