# Archinstaller Edo

## Boot from ISO file

Download the latest ISO file from: https://archlinux.org/download/

Write the ISO file to a USB stick and boot from it (adapt Secure Boot options)

## Authenticate to wi-fi

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
  
The `config.json` file has currently no credentials, during the parameters review before installation, set your disk encryption key, the root password and change the default local user password

### Select which partition to encrypt
  
When the installation process begins you will be asked to select which partition/s need/s to be encrypted, select them with `TAB` and then press `ENTER` 

Then press `ENTER` one last time to start the installation process

## Reboot

Once the installation is done, reboot the system: `reboot`
