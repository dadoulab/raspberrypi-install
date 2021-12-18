# Raspberry Pi 4 Model B Install

## Common commond list

```
sytem report
    - storage
        - RPi


diskutil list
diskutil info -all


sudo raspi-config
sudo apt-get install dnsutils net-tools wget curl

timedatectl list-timezones
timedatectl set-timezone Asia/Shanghai

sudo apt update

sudo nano /etc/environment
export http_proxy="http://username:password@proxy:port"
export https_proxy="http://username:password@proxy:port"
export no_proxy="localhost, 127.0.0.1"

sudo visudo
Defaults env_keep+="http_proxy https_proxy no_proxy"
```

# confirm rpi init ip
nmap -sP 192.168.31.0/24
sudo nmap -sS 192.168.31.108
arp -a


# macos vnc client
cd /System/Library/CoreServices/Applications/
open Screen\ Sharing.app


## REF

* https://www.raspberrypi.com/documentation/computers/configuration.html
* https://www.raspbian.org/RaspbianMirrors
* https://mirrors.tuna.tsinghua.edu.cn/help/raspbian/

Raspberry Pi Headless Setup

* https://desertbot.io/blog/headless-raspberry-pi-4-ssh-wifi-setup
* https://roboticsbackend.com/install-ubuntu-on-raspberry-pi-without-monitor/
