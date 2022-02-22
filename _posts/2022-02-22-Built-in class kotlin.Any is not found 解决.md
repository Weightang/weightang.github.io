---
layout: mypost
title: Built-in class kotlin.Any is not found
categories: [Kotlin]
---
### 前言
最近遇到一个问题，报错kotlin.Any is not found，请求就报错，开始去查看retrofit的源码,发现也正常。后面去网上查找一番，发现在packagingOptions 配置项问题。

### 解决
需要在packagingOptions 上删除 "**/**.kotlin_builtins" "**/*.kotlin_metadata"，**/kotlin/** 的排除项。
在这里做个记录