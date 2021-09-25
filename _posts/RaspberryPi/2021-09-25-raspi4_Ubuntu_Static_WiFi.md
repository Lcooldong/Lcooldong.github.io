---
layout: single
title: Raspberry Pi4 Static WiFi IP

toc: true
toc_sticky: true

date: 2021-09-25
last_modified_at: 2021-09-25
---

Raspi4 version : 20.04.3 LTS focal fossa Ubuntu Server
<br>

{% highlight html %}
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install dhcpcd5
{% endhighlight %}

{% highlight html %}
sudo nano /etc/dhcpcd.conf
{% endhighlight %}

### edit dhcpcd.conf File

{% highlight html %}
interface wlan0
static ip_address=192.168.0.9
static routers=192.168.0.1
static domain_name_servers=192.168.0.1 8.8.8.8 fd51:42f8:caae:d92e::1
static netmask=255.255.255.0
{% endhighlight %}

{% highlight html %}
sudo netplan apply
sudo reboot
{% endhighlight %}



[Go to top](#){: .btn .btn--primary }{: .align-right}