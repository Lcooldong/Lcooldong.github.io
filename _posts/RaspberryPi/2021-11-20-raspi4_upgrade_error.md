---
layout: single
title: Raspberry Pi4 upgrade error

categories : [Raspberry_Pi]
tags : [upgrade]

toc: true
toc_sticky: true

date: 2021-11-20
last_modified_at: 2021-11-20
---


Could not get lock /var/lib/dpkg/lock-frontend
<br>

## Error sentence

{% highlight html %}
Could not get lock /var/lib/dpkg/lock-frontend
{% endhighlight %}
<br>

## Solution

{% highlight html %}
sudo rm /var/lib/apt/lists/lock
sudo rm /var/cache/apt/archives/lock
sudo rm /var/lib/dpkg/lock*
{% endhighlight %}
<br>
{% highlight html %}
sudo dpkg --configure -a
sudo apt-get update
sudo apt-get upgrade
{% endhighlight %}

<br>
[Go to top](#){: .btn .btn--primary }{: .align-right}