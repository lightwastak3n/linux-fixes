# Time and date wrong, not syncing

Network time Protocol is either not installed or not working

Step 1: Install NTP
```bash
sudo pacman -S ntp
```

Step 2: Turn on NTP
```bash
sudo timedatectl set-ntp true
```
