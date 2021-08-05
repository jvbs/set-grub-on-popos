# Set Grub on PopOs

> Run the scripts below in your terminal as root

```bash
sudo apt install grub-efi grub2-common grub-customizer -y

sudo grub-install

sudo cp /boot/grub/x86_64-efi/grub.efi /boot/efi/EFI/pop/grubx64.efi

sudo grub-customizer
```

1. After grub-customizer tool is launched, go to `File` > `Change Environment`
2. Replace `OUTPUT_FILE` configuration with:

```
/boot/efi/EFI/pop/grub.cfg
```

    And check the box `Save this configuration` and apply your settings.

3. Reboot your machine, enter in your BIOS and set `pop` as your default bootloader.

4. Done.
