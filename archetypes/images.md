---
title: "{{ replace .TranslationBaseName "-" " " | title }}"
date: {{ .Date }}
draft: false
type: image
# image is relative to /static/images/
image: {{ .TranslationBaseName }}.jpg
show_title: false
# via: add a URL for attribution if it's not your image
via: 
tags:
---
