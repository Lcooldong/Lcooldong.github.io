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

5. Go to the config file. Write your Raspi4 Ip. : <br>
<br>
Host raspi4_WiFi <br>
&nbsp&nbsp&nbsp&nbsp HostName [Your IP Number] <br>
&nbsp&nbsp&nbsp&nbsp Port 22 <br>
&nbsp&nbsp&nbsp&nbsp User ubuntu <br>
&nbsp&nbsp&nbsp&nbsp IdentityFile ~\.ssh\keys <br>

This is Example of my WiFi Connection. <br>

6. After save config file, press F1, write connect, and click your connection. <br>

7. It will be connected. <br>

<br>
[GO TO TOP](#){: .btn .btn--primary } <br>