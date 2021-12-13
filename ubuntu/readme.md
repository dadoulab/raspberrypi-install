# Ubuntu 20.04 for Raspberry Pi Install

```
// default user
pi:raspberry

// Install Desktop
sudo apt install ubuntu-desktop|xubuntu-desktop

// Install RealVNC
sudo apt-get install -y realvnc-vnc-server realvnc-vnc-viewer
vncserver

// Tightvncserver
sudo apt install tightvncserver
tightvncserver -geometry 1440x900

sudo crontab -e
@reboot su - pi -c '/usr/bin/tightvncserver -geometry 1440x900'

```
