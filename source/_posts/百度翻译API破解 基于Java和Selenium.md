---
layout: java
title: 百度翻译API破解 基于Java和Selenium
date: 2019-02-13 17:05:52
tags:
  - java
  - selenium
thumbnail: https://images.pexels.com/photos/982378/nature-milky-way-galaxy-stars-982378.jpeg
---

在一次偶然的情况下, 我对自己提出了一个需求, 那就是把 数据库的所有表格和字段的名称翻译成中文, 但是一个一个地翻译很浪费时间, 于是就想到了翻译引擎。
虽说翻译引擎都是有提供的API接口, 但是自己同时为了学习一下爬虫就去尝试着破解百度翻译的翻译接口, 然后就有了接下来的故事了... ...
<!--more-->
说干就干, 打开浏览器,打开[百度翻译](https://fanyi.baidu.com/)的界面 F12调出开发人员工具, 然后在Network一栏下, 清空一下最近的请求, 接着就可以开始追接口了:  
在输入框中随便输点什么之后回车, 发现此时Network下有了几条新的请求(可以点击筛选按钮XHR筛选请求):
##### langdetect：https://fanyi.baidu.com/langdetect
##### v2transapi：https://fanyi.baidu.com/v2transapi
当点击langdetect之后, 可以看到Preview/Response一栏中的返回数据, 找到了关键词：zh, 猜测是用来做语言种类识别的  
二点击v2transapi之后, 同样的观察返回数据, 可以确定是

