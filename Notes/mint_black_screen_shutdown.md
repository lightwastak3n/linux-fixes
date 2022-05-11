# Mint doesnt turn off just stays on the black screen after shutdown

Tried different things but this fixed it.

Change the line in `etc/default/grub` from
```bash
GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"
```
to
```bash
GRUB_CMDLINE_LINUX_DEFAULT="quiet splash acpi=off"
```
and then `sudo grub-update`
