---
layout: single
title: Raspberry Pi4 install WiringPi
---

To use "gpio -v" and "gpio readall", we have to install Wiring pi

Follow this on terminal.

before you start, just recommended.
sudo apt-get update
sudo apt-get full-upgrade

1. sudo apt purge wiringpi
2. hash -r
3. git clone https://github.com/WiringPi/WiringPi.git
4. ls <- check there is WiringPi directory
5. cd WiringPi
6. git pull origin
7. sudo apt-get install make
8. ./build

now it's end

-> gpio -v
-> gpio readall

