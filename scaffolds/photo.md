---
title: {{ title }}
date: {{ date }}
categories: [手札, 化語, 跫響, 吟遊, 程設, 寫真]
tags: [手札, 化語, 跫響, 吟遊, 程設, 寫真]
---
{% asset_img {{ date }}.jpg {{ title }} %}

{% img [url] {{ title }} %}

攝於

{% googlemaps [latitude] [longitude] 16 100% 450px %}
  [location], [latitude], [longitude]
{% endgooglemaps %}