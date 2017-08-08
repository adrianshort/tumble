---
title: "{{ replace .TranslationBaseName "-" " " | title }}"
date: {{ .Date }}
draft: false
type: image
# image_filename is relative to /static/images/
image_filename: {{ .TranslationBaseName }}.jpg
show_title: false
tags:
---
