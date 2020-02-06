---
title: 온라인 호스팅 지침
permalink: index.html
layout: 홈
---

# 콘텐츠 디렉터리

각 연습에 대한 하이퍼링크. 강사는 연습을 데모 또는 학생 랩으로 사용할 수 있습니다. 

## 연습

{% assign wts = site.pages | where_exp:"page", "page.url contains '/Instructions/Walkthroughs'" %}
| 모듈 | 연습 |
| --- | --- | 
{% for activity in wts %}| {{ activity.wts.module }} | [{{ activity.wts.title }}{% if activity.wts.type %} - {{ activity.wts.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}

