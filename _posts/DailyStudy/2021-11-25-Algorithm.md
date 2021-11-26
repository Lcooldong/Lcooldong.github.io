---
layout: single
title: 211125_class

categories : [DailyStudy]
tags : [Algorithm]

toc: true
toc_sticky: true

date: 2021-11-25
last_modified_at: 2021-11-25
---

## Stack
<br>
후위법(posfit)  
:연산자를 뒤로 보내는 방법  
90/(2*3)+(20-10) -> ??  
90 2 3 * / 20 10 - +  
<br>
push(), pop()  
{% highlight html %}
스택 사이즈 10개
int top = -1;
void push(int* array, int num){
    if(top >= 9){
        printf("오버플로우\n");
        return;
    }else{
        top=top+1;
        array[top]=num;
    }
}
{% endhighlight %}
<br>
{% highlight html %}
int pop(int* array){
    if(top < 0){
        printf("언더플로우\n");
        return -1;
    }else{
        return array[top--];
    }
}
{% endhighlight %}}
<br>

## Queue

rear(출력 시 index), front(입력 시 index)  
enque(), deque()  
초기위치 : rear=front=-1  
배열 : queue[]  
원형 Queue  

## Linked list

{% highlight html %}
typdef struct _node{
    int key;
    struct _node* next;
} node;
{% endhighlight %}}

