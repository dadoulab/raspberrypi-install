# Raspberry Pi OS Install

```
// boot config
config/ssh
config/wpa_supplicant.conf

// default user
pi:raspberry

// options
sudo nano /etc/sysctl.d/routed-ap.conf
# Enable IPv4 routing
net.ipv4.ip_forward=1

// modify apt source.list
sudo cp /etc/apt/sources.list{,.bak}
sudo cp /etc/apt/sources.list.d/raspi.list{,.bak}

sudo tee /etc/apt/sources.list >/dev/null <<EOF
deb http://mirrors.aliyun.com/raspbian/raspbian/ bullseye main non-free contrib
deb-src http://mirrors.aliyun.com/raspbian/raspbian/ bullseye main non-free contrib
EOF

sudo tee /etc/apt/sources.list.d/raspi.list >/dev/null <<EOF
deb http://mirrors.aliyun.com/raspberrypi/ bullseye main
EOF

sudo apt update && \
  sudo apt upgrade -y && \
  sudo apt-get autoremove -y
```



# REF

https://ubuntu.com/download/raspberry-pi
https://www.youtube.com/watch?v=eeFzXX8q0BM
https://www.youtube.com/watch?v=1OBpT6ppgJU
https://elinux.org/RPiconfig#Video
