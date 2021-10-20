---
layout: single
title: Python QT label and button scope

categories : [python]
tags : [python]

toc: true
toc_sticky: true

date: 2021-10-14
last_modified_at: 2021-10-14
---

Python QT self
<br>

## 1. diffence between self and not self

### example
{% highlight html %}
self.lbl = Qlabel('label1')
btn = Qpushbutton('button1')
{% endhighlight %}

### scope
self.lbl 은 class 변수
btn은 local 변수

### handler
람다는 호출이 아니라 선언하는 것임.
<br>

{% highlight html %}
btn.clicked.connect(lambda: self.lbl.setText('button'))
{% endhighlight %}

handler 가 실행될 때 람다 함수를 호출함.    
그래서 초기화 이후에 self.lbl 에 self를 반드시 사용.  
사라지는 지역변수가 아닌 클래스 변수이다.   

<br>

### lambda
{% highlight html %}
btn.clicked.connect(lambda x=n.text(): self.on_button(x))
{% endhighlight %}
x=n.text() -> default 인자는 init 때 들어감 


[Go to top](#){: .btn .btn--primary }{: .align-right}