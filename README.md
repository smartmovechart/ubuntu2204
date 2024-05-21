# ubuntu2204

## bluetooth
```
sudo apt install --reinstall linux-modules-extra-6.5.0-35-generic

mokutil --sb
sudo apt install git dkms
git clone https://github.com/jeremyb31/bluetooth-5.19.git
sudo dkms add ./bluetooth-5.19
sudo dkms install btusb/4.0
or
sudo dkms install btusb/4.0 --kernelsourcedir=/usr/src/linux-headers-6.5.0-35-generic

sudo apt install linux-generic-hwe-22.04

```
