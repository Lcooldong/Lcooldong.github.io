---
title: "매일공부"
layout: archive
permalink: categories/dailystudy
author_profile: true
sidebar_main: true
---

{% assign posts = site.categories.DailyStudy %}
{% for post in posts %} {% include archive-single2.html type=page.entries_layout %} {% endfor %}

<!-- 눈에 보이는 부분 title (눌렀을 때) -->