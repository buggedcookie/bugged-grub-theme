# Bugged-Grub
![Bugged-Grub Preview](./preview.png)

A personal GRUB theme I created for myself.

The repository includes `bugged-grub.fig`, a Figma project that makes it easy to customize colors, images, and layout elements.

## Installation

Copy the `bugged-grub` folder into your GRUB themes directory:

```bash
sudo cp -r ~/Downloads/bugged-grub-theme/bugged-grub /boot/grub/themes/
```

Alternatively:

```bash
sudo mv ~/Downloads/bugged-grub-theme/bugged-grub /boot/grub/themes/
```

## GRUB Configuration

Edit:

```bash
sudo nano /etc/default/grub
```

Make sure the following options are set correctly:

```bash
GRUB_GFXMODE=2560x1440
GRUB_GFXPAYLOAD_LINUX=keep
GRUB_THEME="/boot/grub/themes/bugged-grub/theme.txt"
```

Replace `2560x1440` with your monitor's native resolution if needed.

## Apply Changes

Regenerate your GRUB configuration:

```bash
sudo grub-mkconfig -o /boot/grub/grub.cfg
```

> **Warning**
>
> Always verify that your GRUB configuration is valid before rebooting. An invalid configuration may prevent GRUB from loading correctly.
>
> If that happens, you may need to boot from a live USB, restore your GRUB configuration, or manually boot your kernel from the GRUB command line.

Reboot and enjoy.
