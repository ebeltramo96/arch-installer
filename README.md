# Archinstaller

## Boot from ISO file

Download the latest ISO file from: https://archlinux.org/download/

Write the ISO file to a USB stick and boot from it (adapt Secure Boot options)

## Authenticate to wi-fi

https://wiki.archlinux.org/title/iwd

`iwctl --passphrase=PASSPHRASE station DEVICE connect SSID`

## Launch archinstaller

### Default configuration

`archinstall --config <path to user config file or URL> --disk-layout <path to disk layout config file or URL> --creds <path to user credentials config file or URL>`

### My configuration

`archinstall --config https://github.com/ebeltramo96/archinstaller/blob/main/user_configuration.json --disk-layout https://github.com/ebeltramo96/archinstaller/blob/main/user_disk_layout.json --creds https://github.com/ebeltramo96/archinstaller/blob/main/user_credentials.json`

### Install git and clone remote repo

`pacman -Sy git --noconfirm`

`git clone https://github.com/ebeltramo96/archinstaller.git /mnt`

### My configuration

`archinstall --config /mnt/user_configuration.json --disk-layout /mnt/user_disk_layout.json --creds /mnt/user_credentials.json`

### Adapt credentials
  
The `user_credentials.json` file has currently no credentials, during the parameters review before installation, set your disk encryption key, the root password and your local user and password

### Select which partition to encrypt:
  
When the installation process begins you will be asked to select which partition/s need/s to be encrypted, select them with `TAB` and then press `ENTER`  

## Reboot

`reboot`
