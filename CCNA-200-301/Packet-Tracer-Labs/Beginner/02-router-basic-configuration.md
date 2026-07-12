# Lab 02: Router Basic Configuration

## Objective

Configure basic router settings and enable connectivity between a PC and a router interface.

## Topology

- 1 router
- 1 switch
- 1 PC

## Addressing Table

| Device | Interface | IP Address | Subnet Mask | Default Gateway |
| --- | --- | --- | --- | --- |
| R1 | G0/0 | 192.168.10.1 | 255.255.255.0 | N/A |
| PC1 | FastEthernet0 | 192.168.10.10 | 255.255.255.0 | 192.168.10.1 |

## Tasks

1. Build the topology.
2. Configure the router hostname as `R1`.
3. Configure the router interface IP address.
4. Enable the router interface.
5. Configure the PC IP settings.
6. Verify connectivity.

## Router Commands

```text
enable
configure terminal
hostname R1
interface g0/0
ip address 192.168.10.1 255.255.255.0
no shutdown
end
write memory
```

## Verification

From PC1:

```text
ping 192.168.10.1
```

On R1:

```text
show ip interface brief
```

## Notes

- Save the completed Packet Tracer file as `02-router-basic-configuration.pkt`.

