# MEDUSA PASSWORD CRACKING 


# Installazione 

```bash
sudo dpkg --configure -a && sudo apt-get install -f && sudo apt-get update
```
```bash
sudo apt-get install linux-headers-$(uname -r) build-essential make patch subversion openssl libssl-dev libncp-dev libpq-dev libgcrypt11-dev libgnutls-dev libsvn-dev zlib1g-dev libssh2-1-dev libnl-dev gettext autoconf tcl8.5 libpcap0.8-dev python-scapy python-dev cracklib-runtime macchanger-gtk tshark ethtool
```
```bash
sudo apt-get install medusa
```
```bash
sudo wget http://www.foofus.net/jmk/tools/medusa-2.1.1.tar.gz -O - | sudo tar -xvz
```
```bash
cd medusa*
```
```bash
./configure
```
```bash
sudo make && sudo make install
```
Per vedere i moduli e le opzioni possibli
```bash
medusa -q
```


```bash

```

