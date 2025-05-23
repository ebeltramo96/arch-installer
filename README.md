<p align="center">
  <img src="https://www.archlinux.org/static/logos/archlinux-logo-dark-1200dpi.b42bd35d5916.png" alt="alt text" width="600" height="200">
</p>

# Arch Installer edo

## Boot from ISO file

Download the latest ISO file from: https://archlinux.org/download/

Write the ISO file to a USB stick and boot from it (adapt Secure Boot options)

## Partitions status

If the laptop's disk has no partitions, skip this step.

In case the disk already has partitions, use `fdisk -l` and delete them, reboot the laptop and restart the installation

## Authenticate to wi-fi

first, switch to bash:

`bash`

then, enter _iwctl_ and list the devices:

`iwctl`

`device list`

https://wiki.archlinux.org/title/iwd

then exit, and connect to the wi-fi:

`iwctl --passphrase PASSPHRASE station DEVICE connect SSID`

## Launch archinstaller

### Install git and clone remote repo

`pacman-key --init`

`pacman -Sy git glibc --noconfirm`

`git clone https://github.com/ebeltramo96/arch-installer.git /mnt`

### My configuration

`archinstall --config /mnt/config.json --disk-layout /mnt/disk.json`

### Adapt credentials
  
The `config.json` file has no credentials, before the installation, check the options and:
- set your disk encryption key
- the root password
- change the default local user password

Now select `Install` to move to the next view

### Start the installation

At this point the final configuration is shown, if it's fine, press `ENTER` to start the installation process

## Reboot

Once the installation is done, reboot the system: `reboot`
