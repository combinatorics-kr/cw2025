---
layout: en
---
# History

{% for item in site.data.history %}
{% assign title=item.year | append: " Combinatorics Workshop" %}
{% assign titleko=item.year | append: "년 조합론 학술대회" %}
{% assign n2=item.n | slice:-2,2 %}
{% assign n1=item.n | slice:-1,1 %}

## {{ item.n }}{%  
    if n1== "1" and n2 != "11" %}st{% 
    elsif n1== "2" and n2 != "12" %}nd{%
    elsif n1 == "3" and n2 != "13" %}rd{%
    else %}th{%
    endif  
%}: [{{ item.title | default: title}}]({{item.url}})
- Korean name: {{ item.titleko | default: titleko}}
- Date: {{ item.dates }}, {{item.year}}
- Venue: {{ item.venue }}, {{ item.city}}
- Host: {{item.host}}
{%- if item.organizer %}
- (Local) Organizers: {{item.organizer}}
{% endif -%}
{% endfor %}
