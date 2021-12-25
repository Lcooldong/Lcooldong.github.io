---
layout: single
title: Make ESP New Project

categories : [ESP32]
tags : [ESP-IDF]

toc: true
toc_sticky: true

date: 2021-12-23
last_modified_at: 2021-12-23
---

## Change CMakeList

1. CMakeList.txt  
{% highlight html %}
include{$ENV{IDF_PATH}/tools/cmake/project.cmake}
project(PROJECT NAME)
{% endhighlight %}
<br>
프로젝트 명 작성

2. main\CMakelists.txt  
{% highlight html %}
idf_component_register(SRCS "CODE.c" INCLUDE DIRS ".")
{% endhighlight %}
<br>
.c 파일과 경로를 나타냄
<br>
테스트 해본 결과 Makefile은 상위 CMake에 의해 사용 안됨