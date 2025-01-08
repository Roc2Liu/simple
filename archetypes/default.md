---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
lastmod: {{ .Date }}
draft: false
author: "{{ .Site.Params.author }}"
description: "本篇文章描述，会用于SEO"
keywords: ["关键词1", "关键词2"]
# 分类和标签
categories: ["默认分类"]
tags: ["默认标签"]
---
