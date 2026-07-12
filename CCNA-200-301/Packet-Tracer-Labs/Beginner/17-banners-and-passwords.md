# Lab 17: Banners and Passwords

## Objective

Configure basic access passwords and warning banners on Cisco devices.

## Topology

- 1 router
- 1 switch
- 1 PC with console access

## Tasks

1. Configure hostnames on the router and switch.
2. Configure an enable secret.
3. Configure console line passwords.
4. Configure VTY line passwords.
5. Encrypt plaintext passwords.
6. Configure a message of the day banner.
7. Save the configuration.

## Example Commands

```text
enable secret class
line console 0
password cisco
login
exit
line vty 0 15
password cisco
login
exit
service password-encryption
banner motd #Authorized users only#
```

## Verification

```text
show running-config
```

## Notes

- Save the completed Packet Tracer file as `17-banners-and-passwords.pkt`.

