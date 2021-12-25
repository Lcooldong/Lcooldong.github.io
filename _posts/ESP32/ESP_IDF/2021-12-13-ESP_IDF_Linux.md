---
layout: single
title: Install ESP_IDF for Linux

categories : [ESP32]
tags : [ESP-IDF]

toc: true
toc_sticky: true

date: 2021-12-13
last_modified_at: 2021-12-13
---

[Youtube Link](https://www.youtube.com/watch?v=Jt6ZDct4bZk)
<br>

## Setup

{% highlight html %}
sudo apt-get install git wget flex bison gperf python3 python3-pip python3-setuptools cmake ninja-build ccache libffi-dev libssl-dev dfu-util libusb-1.0-0
{% endhighlight %}
<br>

## Download

{% highlight html %}
mkdir -p ~/esp
cd ~/esp
git clone --recursive https://github.com/espressif/esp-idf.git
{% endhighlight %}
<br>
--recursive : 하위 서브모듈까지 모두 clone 한다.
<br>

## esp32
{% highlight html %}
cd ~/esp/esp-idf
./install.sh esp32
{% endhighlight %}
<br>
or
<br>
{% highlight html %}
cd ~/esp/esp-idf
./install.fish esp32
{% endhighlight %}

## Run manually
Go to esp-idf  
And, write down  
{% highlight html %}
. export.sh
{% endhighlight %}

## .profile (Run automatically)
{% highlight html %}
. $HOME/(esp-idf path)/export.sh
{% endhighlight %}
In my case,  
{% highlight html %}
. $HOME/Documents/ESP/esp-idf/export.sh
{% endhighlight %}


## Use usb port

For me, I don't need this code because my os is Ubuntu 20.04.  
But, if you use virtual machine, you have to use the code.  
<br>
{% highlight html %}
sudo usermod -a -G dialout,tty $USER
{% endhighlight %}
<br>
And, reboot please.
<br>


## Example

{% highlight html %}
cd ~/esp
cp -r $IDF_PATH/examples/get-started/hello_world .
cd ~/esp/hello_world
idf.py set-target esp32
idf.py menuconfig   <-(if you need)
{% endhighlight %}
<br>

{% highlight html %}
idf.py build
idf.py -p PORT [-b BAUD] flash  [example-> idf.py -p /dev/ttyUSB0 flash]
{% endhighlight %}
<br>