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
## nvidia drivers
sudo ubuntu-drivers install latest


## QEMU/KVM windows

```
sudo apt install qemu virt-manager
```
reboot and change default image storage path to /home/datasets2/virtimages
```
virsh pool-destroy default
virsh pool-undefine default
virsh pool-define-as --name default --type dir --target /home/datasets2/virtimages
virsh pool-start default
virsh pool-autostart default
sudo systemctl restart libvirtd
```
virt-manager to install windows/Linux VMs

<br/>
Follow https://sysguides.com/install-a-windows-11-virtual-machine-on-kvm
