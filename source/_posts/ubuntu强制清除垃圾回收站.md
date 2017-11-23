---
title: ubuntu强制清除垃圾回收站
copyright: true
date: 2017-11-22 20:38:23
tags: [unbuntu,linux，垃圾站]
categories: linux
---
# 强制清除垃圾回收站

<!--more-->
## 问题

我遇到了无法在Ubuntu 16.04中清空回收站的问题。我右键回收站图标并选择清空回收站，就像我一直做的那样。我看到进度条显示删除文件中过了一段时间。但是它停止了,垃圾站中有些文件删除了，但有些文件还是没有删除。在看了文件夹后原来没有权限。

## 方案
Ubuntu 16.04的回收站路径为

```bash
：$HOME/.local/share/Trash/
```
然后用以下命令即可清空回收站

```bash
sudo rm -fr $HOME/.local/share/Trash/files/*
```
