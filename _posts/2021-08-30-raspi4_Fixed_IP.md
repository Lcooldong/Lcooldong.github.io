---
layout : single
title : Raspberry pi4 LAN port communition
---

I use my laptop WiFi to eth0 connected raspberry Pi4.

We use 4 things to do.

1. Putty
2. cmd (window)
3. dhcpcd5
4. Window network Centor


◆ Go to network center and double click wifi.  
  
![net](https://user-images.githubusercontent.com/32934089/131289265-1d2203e4-aecb-4c42-aed2-33e8ada97829.JPG)  

◆ Open cmd
  
->  ipconfig  
![net2](https://user-images.githubusercontent.com/32934089/131289404-c1481287-8663-45e1-b8bb-2ef5fb1cee25.JPG)

-> arp -a  
![net3](https://user-images.githubusercontent.com/32934089/131289550-cd6fb4d5-003c-4bba-8d53-429f59c56b6e.JPG)

I fixed my ip but, you can find 192.168.137.X  (not 255).  

  
◆ Go to putty and connect SSH.   
  
![net4](https://user-images.githubusercontent.com/32934089/131289828-35e203a7-24e6-45ca-beb6-a40499f7857a.JPG)


sudo vim /etc/dhcpcd.conf  or sudo nano /etc/dhcpcd.conf  

![net5](https://user-images.githubusercontent.com/32934089/131290460-56edc04a-844e-4ad1-80ec-5861d47e06d0.JPG)

interface eth0  
statc ip_address=192.168.137.(number what you want not 0 or 1)/24  
static routers=192.168.137.1  
static netmask=255.255.255.0  


After this, reboot raspberry pi.  
And, reconnect ethernet wire.  
Then, open the network center.

◆ Connect your fixed ip.   
  
![net6](https://user-images.githubusercontent.com/32934089/131291088-aaef486a-c352-4520-85a7-7e5ab0e6783f.JPG)

nano save ->    ctrl + s
nano quit ->    ctrl + x
vim insert ->   i or a
vim quit and save -> ESC, :(shift+;)wq

if you don't have vim editor -> sudo apt-get install vim  
if your **dhcpcd.conf** file is empty -> sudo apt-get install dhcpcd5  

◆ tip command   
-> route  
-> ip route  
-> ifconfig




