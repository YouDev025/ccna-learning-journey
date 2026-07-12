# Lab 10: Switch Management SVI

## Objective

Configure a switch virtual interface so the switch can be managed over the network.

## Topology

- 1 switch
- 1 router
- 1 PC

## Addressing Table

| Device | Interface | IP Address | Subnet Mask | Default Gateway |
| --- | --- | --- | --- | --- |
| SW1 | VLAN 1 | 192.168.50.2 | 255.255.255.0 | 192.168.50.1 |
| R1 | G0/0 | 192.168.50.1 | 255.255.255.0 | N/A |
| PC1 | FastEthernet0 | 192.168.50.10 | 255.255.255.0 | 192.168.50.1 |

## Tasks

1. Configure the router interface.
2. Configure the switch SVI.
3. Configure the switch default gateway.
4. Configure the PC IP settings.
5. Ping the switch from the PC.

## Example Commands

```text
interface vlan 1
ip address 192.168.50.2 255.255.255.0
no shutdown
exit
ip default-gateway 192.168.50.1
```

## Notes

- Save the completed Packet Tracer file as `10-switch-management-svi.pkt`.

