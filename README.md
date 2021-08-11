# NVIDIA Driver installation on Elementary OS 6 - Odin

Hello everybody :)

I'm using Elementary OS Odin right now in a machine with a NVIDIA GT 610.

To install my drivers, I'm execute this is steps:

1- Update and upgrade the system:
```shell
sudo apt update && sudo apt full-upgrade -y 
```

2- Next, install kernel headers:
```shell
sudo apt install linux-headers-$(uname -r)
```

3- Now check available drivers to your GPU:
```shell
administrador@MS-7680-6be40ceb:~/Downloads$ sudo ubuntu-drivers devices
WARNING:root:_pkg_get_support nvidia-driver-390: package has invalid Support Legacyheader, cannot determine support level
== /sys/devices/pci0000:00/0000:00:01.0/0000:01:00.0 ==
modalias : pci:v000010DEd0000104Asv00000000sd00000000bc03sc00i00
vendor   : NVIDIA Corporation
model    : GF119 [GeForce GT 610]
driver   : nvidia-340 - distro non-free
driver   : nvidia-driver-390 - distro non-free recommended
driver   : xserver-xorg-video-nouveau - distro free builtin
```
4- Next, install recommended version (In my case is 390)
```shell
sudo apt install nvidia-driver-390
```

5- Last, reboot :)

After all, everything will works fine.
