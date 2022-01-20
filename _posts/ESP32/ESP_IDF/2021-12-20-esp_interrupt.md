---
layout: single
title: ESP_IDF interrupt

categories : [ESP32]
tags : [ESP-IDF]

toc: true
toc_sticky: true

date: 2021-12-20
last_modified_at: 2021-12-20
---

[ESP_IDF Github](https://github.com/espressif/esp-idf)
<br>
In this github file, you can find example folder.
<br>

## INPUT interrupt 설정

GPIO_INT_TYPE  

GPIO_PIN_INTR_DISABLE = 0; -> 사용안함  
GPIO_PIN_INTR_POSEDGE = 1; -> RISING Edge  (0 -> 1)  
GPIO_PIN_INTR_NEGEDGE = 2; -> Falling Edge (1 -> 0)  
GPIO_PIN_INTR_ANYEDGE = 3; -> 아무 거나 발동  
GPIO_PIN_INTR_LOLEVEL = 4; -> LOW 일정 시간 유지 시 발동  
GPIO_PIN_INTR_HILEVEL = 5; -> HIGH 일정 시간 유지 시 발동  
<br>

사용 예)  
{% highlight html %}
gpio_config_t io_conf;  // 구조체 선언
io_conf.intr_type = GPIO_PIN_INTR_POSEDGE;  // 사용 방식
{% endhighlight %}
<br>

## isr

Interrupt Service Routine : Interrupt Handler  

1. 인터럽트 핀 설정 : gpio_set_intr_type  
2. 저장할 QUEUE 생성  
3. 인터럽트 발생 시 구현 함수(isr은 아님) 연동  
4. 인터럽트 서비스 시작 코드 : gpio_install_isr_service  
5. 인터럽트 추가 : isr_handlder_add  

<br>
[Go to top](#){: .btn .btn--primary }{: .align-right}