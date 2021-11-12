---
layout: single
title: 2. ESP32 Interrupt and Timer

categories : [ESP32]
tags : [tutorials, interrupt]

toc: true
toc_sticky: true

date: 2021-11-10
last_modified_at: 2021-11-10
---

# ESP32 Interrupt and Timer
<br>

[Tutorials_Site](https://randomnerdtutorials.com/esp32-pir-motion-sensor-interrupts-timers/)
<br>


  
## Interrupt
{% highlight html %}
attachInterrupt(digitalPinToInterrupt(GPIO), function, mode);
{% endhighlight %}
<br>

### Error
{% highlight html %}
Guru Meditation Error: Core  1 panic'ed (Interrupt wdt timeout on CPU1). 

Core  1 register dump:
PC      : 0x4008a07a  PS      : 0x00060635  A0      : 0x80089546  A1      : 0x3ffbed20  
A2      : 0x3ffb8a00  A3      : 0x3ffb8890  A4      : 0x00000004  A5      : 0xb33fffff  
A6      : 0x00000001  A7      : 0x00000001  A8      : 0x3ffb8890  A9      : 0x00000018  
A10     : 0x3ffb8890  A11     : 0x00000018  A12     : 0x3ffc17fc  A13     : 0xb33fffff  
A14     : 0x00000001  A15     : 0x00000001  SAR     : 0x0000000a  EXCCAUSE: 0x00000006  
EXCVADDR: 0x00000000  LBEG    : 0x40085f95  LEND    : 0x40085fa5  LCOUNT  : 0xfffffffb  
Core  1 was running in ISR context:
EPC1    : 0x400d8ad7  EPC2    : 0x00000000  EPC3    : 0x00000000  EPC4    : 0x00000000

Backtrace:0x4008a077:0x3ffbed200x40089543:0x3ffbed40 0x400886bb:0x3ffbed60 0x400d1fe7:0x3ffbeda0 0x400d154d:0x3ffbedc0 0x400d1777:0x3ffbede0 0x400d179d:0x3ffbee00 0x40081109:0x3ffbee20 0x400d1079:0x3ffbee40 0x400840b1:0x3ffbee60 0x400882a2:0x3ffb2770 0x400d1e91:0x3ffb27b0 0x400d14d1:0x3ffb27e0 0x400d1569:0x3ffb2800 0x400d1b92:0x3ffb2820 

Core  0 register dump:
PC      : 0x4008a204  PS      : 0x00060035  A0      : 0x80088e89  A1      : 0x3ffbe7d0  
A2      : 0x3ffbee78  A3      : 0x3ffbe7ec  A4      : 0x00060023  A5      : 0xb33fffff  
A6      : 0x0000cdcd  A7      : 0x0000abab  A8      : 0x0000abab  A9      : 0x0000abab  
A10     : 0x00000000  A11     : 0x00000000  A12     : 0x3ffc1608  A13     : 0x00000007  
A14     : 0x00000005  A15     : 0x00000001  SAR     : 0x0000001a  EXCCAUSE: 0x00000006  
EXCVADDR: 0x00000000  LBEG    : 0x00000000  LEND    : 0x00000000  LCOUNT  : 0x00000000  

Backtrace:0x4008a201:0x3ffbe7d00x40088e86:0x3ffbe810 0x40087da3:0x3ffbe830 0x40087af9:0x3ffbe850 0x400840b9:0x3ffbe860 0x400ebb23:0x3ffbd840 0x400d7be6:0x3ffbd860 0x40088a51:0x3ffbd880 

ELF file SHA256: 0000000000000000

Rebooting...
ets Jun  8 2016 00:22:57

rst:0xc (SW_CPU_RESET),boot:0x13 (SPI_FAST_FLASH_BOOT)
configsip: 0, SPIWP:0xee
clk_drv:0x00,q_drv:0x00,d_drv:0x00,cs0_drv:0x00,hd_drv:0x00,wp_drv:0x00
mode:DIO, clock div:1
load:0x3fff0030,len:1420
ho 0 tail 12 room 4
load:0x40078000,len:13540
load:0x40080400,len:3604
entry 0x400805f0
{% endhighlight %}

[HINT_for_my_Solution](https://forum.arduino.cc/t/esp32-guru-meditation-error-core-1-paniced-coprocessor-exception/596231)

I think many signals make error.  
So, I use add only 
{% highlight html %}
delay(1)
{% endhighlight %}
to stop interrupt. (in void loop())
<br>


## Timer
{% highlight html %}
delay(time in milliseconds)
{% endhighlight %}
{% highlight html %}
millis()
{% endhighlight %}
<br>

## Timer Interrupt
{% highlight html %}
const long interval = 1000; 
unsigned long currentMillis = millis();
if (currentMillis - previousMillis >= interval) {
    previousMillis = currentMillis;
}
{% endhighlight %}


<br>
[Go to top](#){: .btn .btn--primary }{: .align-right}