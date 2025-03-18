---
layout: ko
---
# 역사

{% for item in site.data.history %}
{% assign title=item.year | append: " Combinatorics Workshop" %}
{% assign titleko=item.year | append: " 조합론 학술대회" %}

## {{ item.n }}회: [{{ item.titleko | default: titleko}}]({{item.url}})
- 영문 이름: {{ item.title | default: title}}
- 날짜: {{ item.dates }}, {{item.year}}
- 장소: {{ item.venue }}, {{ item.city}}
- Host: {{item.host}}
{%- if item.organizerko %}
- 주관/운영위원: {{item.organizerko}}
{% endif -%}
{% endfor %}
