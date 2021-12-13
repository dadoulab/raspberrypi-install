# Raspberry Pi 4 Model B Install

## Common commond list

```
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

## Issues

* Can You Check from Raspbian?

```
dmesg
rev 1.2?

cat /proc/cpuinfo
Revision: b03112(Rev 1.2 board)
Revision: b03111(Rev 1.1 board)
```

* Bullseye vncserver is very slow without display?

https://forums.raspberrypi.com/viewtopic.php?t=323294

```
vim /boot/config.txt
#dtoverlay=vc4-kms-v3d

vim /boot/cmdline.txt
video=HDMI-A-1:1920x1080@60D
```

## REF

* https://www.raspberrypi.com/documentation/computers/configuration.html
* https://www.raspbian.org/RaspbianMirrors
* https://mirrors.tuna.tsinghua.edu.cn/help/raspbian/

Raspberry Pi Headless Setup

* https://desertbot.io/blog/headless-raspberry-pi-4-ssh-wifi-setup
* https://roboticsbackend.com/install-ubuntu-on-raspberry-pi-without-monitor/
