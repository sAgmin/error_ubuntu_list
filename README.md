# error_ubuntu_list

## Table
1. [Ubuntu 18.04 기준 이더넷 (Wifi 아님) 인식이 안되는 현상] (#Ubuntu-18.04-기준-이더넷-(Wifi-아님)-인식이-안되는-현상)

## WSL2

### How to install Anaconda on wsl
아나콘다 홈페이지에서 직접 다운로드하는 것보다 아래처럼 wget을 사용하는 것이 편함
Download:
```
wget https://repo.anaconda.com/archive/Anaconda3-2021.04-Linux-x86_64.sh	
```
Install:
```
bash Anaconda3-2021.04-Linux-x86_64.sh
```
* https://repo.anaconda.com/archive/ 에서 원하는 버전을 찾을 수 있음* 
## Errors Of Ubuntu
### 기본적인 Ubuntu 문제 해결방법
Try:
```
sudo reboot
```
### Ubuntu 18.04 기준 이더넷 (Wifi 아님) 인식이 안되는 현상

LAN선을 인식은 하고 있는지 확인
```
sudo lshw -C network
```
description: Wireless interface -> Wifi

description: Ethernet interface -> LAN -> 이게 보이면 인식은 하고 있다는 것!

1. product check
Ex) Realtek Semiconductor Co., Ltd.

2. 해당 회사홈페이지에서 LAN Driver install
Ex) https://www.realtek.com/en/component/zoo/category/network-interface-controllers-10-100-1000m-gigabit-ethernet-pci-express-software

3. 재시작
```
service networking restart
```
or
```
sudo reboot
```

