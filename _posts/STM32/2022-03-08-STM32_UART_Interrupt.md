---
layout: single
title: STM32 UART Interrupt

categories : [STM32]
tags : [STM32, interrupt]

toc: true
toc_sticky: true

date: 2022-03-08
last_modified_at: 2022-03-08
---





원하는 바이트 크기보다 더 큰 것을 받았을 경우
내가 처음에 보낸 것은 <CR><LF>가 붙어있어서
일정 크기만큼 잘린 후 버퍼에 남은 것 때문에 먹통이 되어버린 것이다.