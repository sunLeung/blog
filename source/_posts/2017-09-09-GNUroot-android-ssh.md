---
title: GNUroot debian android ssh设置
date: 2017-09-09 21:18:43
tags: gnuroot debian 
categories: technology
---

## SSH设置
```
# 安装openssh
apt-get install openssh-server
# 打开文件/etc/ssh/sshd_conifg,设置一下属性
PermitRootLogin yes 
UsePAM no
UsePrivilegeSeparation no 
```

## 设置语言环境
```
# 查看语言库
locale -a
# 安装locales
apt-get install locales
# 设置环境变量vi ~/.bash_profile
LANG="zh_CN.UTF-8"
LC_ALL="zh_CN.UTF-8"
export LANG
export LC_ALL
# 生效
source .bash_profile
```

## 设置时间同步
```
# 时间（时区）查看
date -R
# 安装时间同步程序
apt-get install ntpdate
# 同步时间
ntpdate time.nist.gov
# 选择时区（只是选择，选择后的结果需要copy到环境变量）
tzselect
# 设置环境变量vi ~/.bash_profile
TZ='Asia/Shanghai'; export TZ
```

## 命令别名
```
# 设置环境变量vi ~/.bash_profile
alias l='ls -alhF'
alias la='ls -AFh'
alias ll='ls -lhAF'
```

