# Lab 24: Small Office LAN

## Objective

Build a small office LAN with PCs, a printer, and a server.

## Topology

- 1 switch
- 3 PCs
- 1 printer
- 1 server

## Addressing Plan

| Device | IP Address |
| --- | --- |
| Server | 192.168.40.10 |
| Printer | 192.168.40.20 |
| PC1 | 192.168.40.101 |
| PC2 | 192.168.40.102 |
| PC3 | 192.168.40.103 |

Use subnet mask `255.255.255.0` for all devices.

## Tasks

1. Build the topology.
2. Configure static IP addresses.
3. Enable HTTP service on the server.
4. Test PC connectivity to the server.
5. Test PC connectivity to the printer.

## Verification

```text
ping 192.168.40.10
ping 192.168.40.20
```

## Notes

- Save the completed Packet Tracer file as `24-small-office-lan.pkt`.

