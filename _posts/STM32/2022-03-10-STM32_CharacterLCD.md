---
layout: single
title: STM32 Character LCD

categories : [STM32]
tags : [STM32, LCD]

toc: true
toc_sticky: true

date: 2022-03-10
last_modified_at: 2022-03-10
---

## 1602 Character LCD

### 4PINS I2C  
1. SCL -> PB8  
2. SDA -> PB9  
3. VCC -> 5V  
4. GND  

SCL(Serial Clock)  
START : HIGH -> LOW  
END   : LOW  -> HIGH  
데이터 송수신은 SCL이 LOW 일때 가능
<br>  
SDA(Serial Data)  


### I2C 란?

Inter Intergrated Circuit
<br>
마스터(master) 1개, 여러 개의 슬레이브(slave)  
반이중(Half-Duplex) 방식 : 송신과 수신이 동시에 불가능  
각각의 슬레이브 주소로 데이터를 전송  


###