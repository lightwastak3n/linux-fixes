# initramfs unpacking failed
Got this after an update on Manjaro.
Same as this - https://forum.manjaro.org/t/initramfs-unpacking-failed-invalid-magic-as-start-of-compressed/137451

Steps that solved it:
1. Download Manjaro ISO and make bootable USB
2. Boot into USB and run `su`
3. `manjaro-chroot -a` - then choose your broken Manjaro
4. `nano /etc/mkinitpcio.conf`  - uncomment the compression gzip line and save
5. `mkinicpio -P && update-grub`
6. Reboot
