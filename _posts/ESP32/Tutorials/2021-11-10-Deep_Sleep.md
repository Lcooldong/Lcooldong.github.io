---
layout: single
title: 3. ESP32 Deep Sleep

categories : [ESP32]
tags : [tutorials, Deep Sleep]

toc: true
toc_sticky: true

date: 2021-11-11
last_modified_at: 2021-11-12
---

# ESP32 Deep Sleep
<br>

[Tutorials_Site](https://randomnerdtutorials.com/esp32-deep-sleep-arduino-ide-wake-up-sources/)
<br>

## Power Mode

1. Active mode  
2. Modem Sleep mode  
3. Light Sleep mode  
4. Deep Sleep mode  
5. Hibernation mode  
<br>
  
## Wake Up Sources
1. Timer
2. Touch pins
3. ULP co-processor
4. external wake up


## Timer Wake Up
{% highlight html %}
esp_sleep_enable_timer_wakeup(time_in_us)
{% endhighlight %}
<br>
time_in_us <- microSeconds  
5㎲ * 1,000,000 = 5 s  
<br> 

## RTC memory
{% highlight html %}
RTC_DATA_ATTR int bootCount = 0;
{% endhighlight %}
<br>

## Deep Sleep start
{% highlight html %}
esp_deep_sleep_start()
{% endhighlight %}
<br>
<br>

## Touch Wake UP

### Sensitivity
{% highlight html %}
#define Threshold 40
{% endhighlight %}
<br>

### Get touchPin status
{% highlight html %}
touchPin = esp_sleep_get_touchpad_wakeup_status();
{% endhighlight %}
<br>
T0 ~ T9
<br>


### Setup touch interrupt
{% highlight html %}
touchAttachInterrupt(T3, callback, Threshold); 
{% endhighlight %}
<br>
T3 -> GPIO15
<br>
callback function  
1. asleep -> not working
2. awake -> hold the touchPin -> working


### Confirm touch
{% highlight html %}
esp_sleep_enable_touchpad_wakeup();
{% endhighlight %}
<br>

## External Wake Up

### BitMask
{% highlight html %}
#define BUTTON_PIN_BITMASK 0x200000000
{% endhighlight %}
<br>
bitmask -> Pin binary registry -> hex
<br>

### ext0
{% highlight html %}
esp_sleep_enable_ext0_wakeup(GPIO_NUM_X, level);
{% endhighlight %}
<br>
onePin and (HIGH or LOW)
<br>

### ext1
{% highlight html %}
esp_sleep_enable_ext1_wakeup(BUTTON_PIN_BITMASK,ESP_EXT1_WAKEUP_ANY_HIGH);
{% endhighlight %}
<br>
BITMASK -> Serveral Pins  
ESP_EXT1_WAKEUP_ANY_HIGH -> Press any button to High 
<br>





<br>
[Go to top](#){: .btn .btn--primary }{: .align-right}