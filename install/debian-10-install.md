# Install script 
```bash
# Prepare
mkdir install && cd install
START_DIR=( pwd )

# Some basic tools
sudo apt install -y wget curl

# Java related
sudo apt install -y default-jdk
sudo apt install -y maven

# Node JS related
# Install the latest version of nodejs using NVM
cd $START_DIR
mkdir nodejs && cd nodejs

curl -sL https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh -o install_nvm.sh
bash install_nvm.sh
source ~/.profile
nvm ls-remote
nvm install 14.18.1
nvm use 14.18.1
# Select node version
# nvm ls
# nvm alias default 14.18.1
# nvm use default

# Python related
python3 -m venv --system-site-packages notebook  

```

# VPN
## IPSec over L2TP
```bash
sudo apt-get -y install network-manager-l2tp
sudo apt-get -y install network-manager-l2tp-gnome
```
## OpenVPN
```bash
sudo apt -y install network-manager-openvpn network-manager-openvpn-gnome
```