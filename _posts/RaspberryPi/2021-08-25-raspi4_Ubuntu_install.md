---
layout: single
title: Raspberry Pi4 Ubuntu Server install.

toc: true
toc_sticky: true

date: 2021-08-25
last_modified_at: 2021-09-07
---

For my ESP project, I want my own Server. <br>

AWS and Google cloud need to pay for making server. <br>

But, raspi 4 doesn't need to care after install. <br>

**Here is image file for Raspi.**  <br>
<https://ubuntu.com/download/raspberry-pi> <br>

Raspberry pi Imager, it's too slow to burn a SD card. <br>

So, I found one program that most people recommended. <br> 
<https://www.balena.io/etcher/> <br>

Install it, you can easily use it. <br>

When SD card has burned, <br>

1. Reconnet your SD card. And go to boot folder. (Only press cancel when warning occur)

2. Make a new file, and change name to "ssh". (No Filename Extension)

3. Open file name "network-config" with notepad++ or any editor, and write your wifi config. <br>
<br>
NOTEPAD : <https://notepad-plus-plus.org/downloads/> <br>
<br>
![wifiset](https://user-images.githubusercontent.com/32934089/132329846-e6e347bc-4b36-4e26-acef-f0d212ca8cee.JPG) <br>



4. Open file name "user-data", add 2 sentence. <br>
<br>
![2sen](https://user-images.githubusercontent.com/32934089/132329735-7c50363e-90b3-45fe-9cec-dd2e1c6884e8.JPG) <br>

5. Insert SD card, turn on your Raspi4, and wait about 2 minutes. <br>

6. Go to your WiFi manager, and you can see ubuntu connected. <br>

7. Turn off your Raspi4, and reconnect. <br>

8. Open putty and connect using your wifi. <br>

9. Login (ID: ubuntu, passwd: ubuntu), and reset your passwd. <br>

10. Reconnect, and done. <br>

<br>
[Go to top](#){: .btn .btn--primary }{: .align-right}
