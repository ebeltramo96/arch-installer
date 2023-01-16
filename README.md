# Archinstaller

## Boot from ISO file

Download the latest ISO file from: https://archlinux.org/download/

Write the ISO file to a USB stick and boot from it (adapt Secure Boot options)

## Authenticate to wi-fi

https://wiki.archlinux.org/title/iwd

`iwctl station DEVICE connect SSID`

## Verify key

## Launch archinstaller

`archinstall --config <path to user config file or URL> --disk-layout <path to disk layout config file or URL> --creds <path to user credentials config file or URL>`

`archinstall --config https://github.com/ebeltramo96/archinstaller/blob/main/user_configuration.json --disk-layout https://github.com/ebeltramo96/archinstaller/blob/main/user_disk_layout.json --creds https://github.com/ebeltramo96/archinstaller/blob/main/user_credentials.json`

### Adapt credentials
  
The credentials file has default credentials, between "" set your disk encryption password, your default user and his password

### Select which partition to encrypt:
  
When the installation process begins you will be asked to select which partition/s need/s to be encrypted, select them with `TAB` and then press `ENTER`  

## Reboot

`reboot`
