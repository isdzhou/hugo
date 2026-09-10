---
title: "{{ replace .File.ContentBaseName "-" " " | title }}"
date: {{ .Date }}
slug: "{{ substr (crypto.MD5 (now.UnixNano | string)) 0 8 }}"
draft: false
tags: []
categories: []
description: ""
---