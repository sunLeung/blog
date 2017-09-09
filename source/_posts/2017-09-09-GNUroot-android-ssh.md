---
title: GNUroot debian android ssh设置
date: 2017-09-09 21:18:43
tags: gnuroot debian 
categories: technology
---

## GNUroot debian android SSH设置

打开文件/etc/ssh/sshd_conifg
设置属性
```
UsePAM no
UsePrivilegeSeparation no 
```