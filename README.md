# error_ubuntu_list
Ubuntu 18.04 기준 

# 목차
[이더넷 (Wifi 아님) 인식이 안되는 현상] (#이더넷-인식이-안되는-현상)

## 기본적인 Ubuntu 문제 해결방법
Try:
```
sudo reboot
```
## 이더넷 인식이 안되는 현상

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

