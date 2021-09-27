---
layout: single
title: Raspberry Pi4 install Miniconda3

categories : [Raspberry_Pi]
tags : [Raspberry_Pi, miniconda]

toc: true
toc_sticky: true

date: 2021-09-25
last_modified_at: 2021-09-25
---

Raspi4 version : 20.04.3 LTS focal fossa Ubuntu Server
<br>
Raspi4 type :  Raspberry Pi 4B 8GB  -> 64-bit aarch64 (arm64)
<br>

{% highlight html %}
sudo apt-get update
sudo apt-get upgrade
{% endhighlight %}

{% highlight html %}
cat /proc/version
cat /etc/os-release
{% endhighlight %}


## download miniconda

[Miniconda Mirror site]<https://repo.anaconda.com/miniconda/> <br>
{% highlight html %}
wget http://repo.continuum.io/miniconda/Miniconda3-latest-Linux-aarch64.sh
{% endhighlight %}

## when lock error occur

change localhost -> "your hostname"
{% highlight html %}
sudo cat /etc/hostname
sudo cat /etc/hosts
sudo nano /etc/hosts
{% endhighlight %}

## install miniconda

{% highlight html %}
sudo md5sum Miniconda3-latest-Linux-aarch64.sh
{% endhighlight %}

{% highlight html %}
sudo /bin/bash Miniconda3-latest-Linux-aarch64.sh
{% endhighlight %}

## miniconda file path

**path -> /home/ubuntu/miniconda3 (ubuntu is username)**
<br>
And, everything is "yes".

{% highlight html %}
sudo nano /home/ubuntu/.bashrc
{% endhighlight %}

<br>

Go to buttom and find or add miniconda PATH.
{% highlight html %}
export PATH="/home/ubuntu/miniconda3/bin:$PATH"
{% endhighlight %}

## Apply change
{% highlight html %}
source ~/.bashrc
{% endhighlight %}

[Go to top](#){: .btn .btn--primary }{: .align-right}