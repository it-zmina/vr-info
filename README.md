# vr-info

## Applications for PC

- scrcpy: https://github.com/Genymobile/scrcpy
- side quest: https://sidequestvr.com/setup-howto
- 4K Video Downloader: https://www.4kdownload.com/products/product-videodownloader

## 

1. Open scrcpy application at PC.
1. At joined Oculus Application click Settings -> Joined Device -> Switch OFF developer mode.
1. Plug USB--USB-C cable into VR helm and PC.
1. At VR helm should appeared confirmation dialog.
1. At Oculus Application switch ON developer mode.
1. At VR helm accept confirmation dialog.
1. Command `adb devices` should show just connected device at list of attached devices

After connecting VR helm by cable at developer mode for streaming helm content execute command
`scrcpy -c 1600:1200:0:200`

## Connect Oculus Quest to PC remotely in developer mode

1. Connect VR help in developer mode by cable.
1. enter `adb tcpip 5555` to put your quest into networked adb mode
1. enter `adb shell ip route` and find out your quests ip address
1. enter `.\adb connect <ipaddress>:5555` use the ip you found out in the former step here
1. unplug your quest

After connecting VR helm remotely at developer mode for streaming content execute command
`scrcpy -p 5555 -c 1600:1200:0:200`

## Devices info

Oculus Quest resolution: 1440 x 1600
Oculus Quest 2 resolution: 1832 x 1920
Oculus Go resolution: 1280 x 1440

## MISC
### Unblock installing for Ubuntu 19
```
sudo sed -i -re 's/([a-z]{2}\.)?archive.ubuntu.com|security.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list

sudo apt-get update && sudo apt-get dist-upgrade
```

### Add an SSH Key to git account

#### Generating public and private keys
1. Open the terminal app on your computer
1. Enter the following command, substituting "example@gmail.com" with you email address
 and "example" with file name for identification content.
1. `ssh-keygen -t rsa -b 4096 -C "example@gmail.com" -f ~/.ssh/example`
1. Enter a secure passphrase
1. To display the contents of your public key enter `cat ~/.ssh/example.pub`
1. Copy the contents of your key to clipboard 

#### Add an PUBLIC SSH Key to your Github Account

1. Log into your GitHub account.
1. Click your avatar and choose **Settings**
1. Select **SSH and GPG keys**
1. Click **New SSH key**
1. At form **SSH keys /Add new** enter a title in the field **Title**
1. At form **SSH keys /Add new** paste your public key into the **Key** field
1. Click **Add SSH key**

> **_NOTE:_**
To add SSH protocol (Secure login and file transfer protocol) update your remote link with command
 `git remote set-url origin git@github.com:it-zmina/vr-info.git`
The valid link for SSH protocol is at github webpage: Code -> Clone dialog -> SSH tab
