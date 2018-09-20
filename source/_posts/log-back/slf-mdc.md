---
title: slf mdc使用
date: 2018-09-20
categories: log-back
tags:
- mdc
---

###MDC介绍

MDC（Mapped Diagnostic Context 映射调试上下文）是Log4j与logback
提供的一种方便在多线程条件下记录日志的功能。

MDC可以认为是一个与当前线程绑定的哈希表， 可以在其中存储键值对，MDC的内容可以
被同一线程中执行的代码所访问， 当前线程的子线程会继承其父线程中的MDC内容

###MDC使用

MDC一般用户存储userID，userName

1. 一是用于日志记录
1. 二是可以在Rest中方便获取当前处理人

使用AOP工具，在用户访问时，获取当前session数据， 从中获取到userId、userName，存入到MDC中

若当前用户未登录，记得调用MDC.clear(),否则就可以读取到之前的数据

也可使用@Around切面，当访问结束时，调用MDC.clear()清空MDC内容。