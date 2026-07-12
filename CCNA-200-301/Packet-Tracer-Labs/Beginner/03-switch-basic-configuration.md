# Lab 03: Switch Basic Configuration

## Objective

Configure basic switch settings, secure access, and verify the switch configuration.

## Topology

- 1 switch
- 1 PC
- Console cable

## Tasks

1. Connect to the switch using the console cable.
2. Configure the hostname as `SW1`.
3. Configure console and privileged EXEC passwords.
4. Encrypt plaintext passwords.
5. Configure a login banner.
6. Save the running configuration.

## Example Commands

```text
enable
configure terminal
hostname SW1
enable secret class
line console 0
password cisco
login
exit
service password-encryption
banner motd #Authorized access only#
end
write memory
```

## Verification

```text
show running-config
show startup-config
```

## Notes

- Save the completed Packet Tracer file as `03-switch-basic-configuration.pkt`.

