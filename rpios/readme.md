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
```
