# Lab 05: DHCP Server on Router

## Objective

Configure a Cisco router as a DHCP server for a LAN.

## Topology

- 1 router
- 1 switch
- 3 PCs

## Addressing

| Device | Interface | IP Address |
| --- | --- | --- |
| R1 | G0/0 | 192.168.30.1/24 |

## Tasks

1. Configure the router LAN interface.
2. Exclude reserved addresses from the DHCP pool.
3. Create a DHCP pool for the LAN.
4. Configure PCs to use DHCP.
5. Verify assigned addresses.

## Example Commands

```text
ip dhcp excluded-address 192.168.30.1 192.168.30.20
ip dhcp pool LAN30
network 192.168.30.0 255.255.255.0
default-router 192.168.30.1
dns-server 8.8.8.8
```

## Verification

```text
show ip dhcp binding
show ip dhcp pool
```

## Notes

- Save the completed Packet Tracer file as `05-dhcp-server-on-router.pkt`.

