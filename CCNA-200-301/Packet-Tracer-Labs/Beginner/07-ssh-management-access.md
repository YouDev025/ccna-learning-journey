# Lab 07: SSH Management Access

## Objective

Configure secure remote management access using SSH.

## Topology

- 1 switch
- 1 PC

## Addressing Table

| Device | Interface | IP Address | Subnet Mask | Default Gateway |
| --- | --- | --- | --- | --- |
| SW1 | VLAN 1 | 192.168.1.2 | 255.255.255.0 | 192.168.1.1 |
| PC1 | FastEthernet0 | 192.168.1.10 | 255.255.255.0 | 192.168.1.1 |

## Tasks

1. Configure the switch hostname.
2. Configure a domain name.
3. Create a local username and secret.
4. Generate RSA keys.
5. Enable SSH on VTY lines.
6. Test SSH access from the PC.

## Example Commands

```text
hostname SW1
ip domain-name ccna.local
username admin secret Cisco123
crypto key generate rsa
ip ssh version 2
line vty 0 15
login local
transport input ssh
```

## Notes

- Save the completed Packet Tracer file as `07-ssh-management-access.pkt`.

