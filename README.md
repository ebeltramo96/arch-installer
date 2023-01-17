<p align="center">
  <img src="https://www.archlinux.org/static/logos/archlinux-logo-dark-1200dpi.b42bd35d5916.png" alt="alt text" width="600" height="200">
</p>

# Arch Installer edo

## Boot from ISO file

Download the latest ISO file from: https://archlinux.org/download/

Write the ISO file to a USB stick and boot from it (adapt Secure Boot options)

## Authenticate to wi-fi

first, switch to bash:

`bash`

https://wiki.archlinux.org/title/iwd

`iwctl --passphrase=PASSPHRASE station DEVICE connect SSID`

## Launch archinstaller

### Install git and clone remote repo

`pacman -Sy git --noconfirm`

`git clone https://github.com/ebeltramo96/archinstaller.git /mnt`

### My configuration

`archinstall --config /mnt/config.json --disk-layout /mnt/disk.json`

P.S. (the installer could fail at this step in case the disk is already partitioned, use `fdisk` to delete them)

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
