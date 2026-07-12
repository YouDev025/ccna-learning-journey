# Lab 13: Save, Backup, and Restore Configuration

## Objective

Practice saving device configurations and backing them up to a server.

## Topology

- 1 router
- 1 switch
- 1 server
- 1 PC

## Tasks

1. Configure basic settings on the router and switch.
2. Save the running configuration to startup configuration.
3. Configure a TFTP server.
4. Copy the router configuration to the TFTP server.
5. Copy the switch configuration to the TFTP server.
6. Review the saved configuration files on the server.

## Useful Commands

```text
write memory
copy running-config startup-config
copy running-config tftp
show startup-config
```

## Questions

- What is the difference between running-config and startup-config?
- Why should network device configurations be backed up?

## Notes

- Save the completed Packet Tracer file as `13-save-backup-and-restore-config.pkt`.

