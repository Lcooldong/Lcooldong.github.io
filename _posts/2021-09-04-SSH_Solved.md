---
layout : single
title : Visual Studio Code Remote Connection.
---

After I touch something about SSH, I can't use my VSC Remote-SSH. <br>

So, I erase everything about SSH in the Raspberry Pi and Window PC. <br>

Last post : <https://lcooldong.github.io/SSH_ERROR/> <br>

I can use Putty again, but still I can't use VSC. <br>

Therefore, I found some solution. <br>

1. I download VSC Extensions: Remote-SSH. <br>

2. Press F1, write "ssh open", and click. <br>

3. Then, you can see "C:\Users\[your User Name]\.ssh\config" <br>

4. Open Puttygen, press "Generate Button", and press "Save public key" on your  "~\.ssh\config"  folder. <br> 

5. Go to the config file. Write your Raspi4 Ip. :

Host raspi4_WiFi <br>
    HostName [Your IP Number] <br>
    Port 22 <br>
    User ubuntu <br>
    IdentityFile ~\.ssh\keys <br>

This is Example of my WiFi Connection.



<br>
[GO TO TOP](#){: .btn .btn--primary } <br>