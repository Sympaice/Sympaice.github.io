---
title: Android手机使用termux高速下载百度云
date: 2018-11-12 19:29:25
tags:
---
<h3>配置</h3><br>
&emsp;&emsp;首先，下载并安装 [termux](https://www.coolapk.com/apk/com.termux),打开并等待termux初始化加载成功，不过速度比较缓慢，可以科学上网提高加载速度。
配置完毕后按顺序输入下面命令,每输入一条都要回车：

<h5>①
```sh
apt update && apt upgrade -y
```
<h5>②
```sh
apt install zip wget -y
```
<h5>③
```sh
termux-setup-storage
```
<h5>④
```sh
wget -O 1.zip https://github.com/iikira/BaiduPCS-Go/releases/download/v3.5.6/BaiduPCS-Go-v3.5.6-android-21-arm64.zip
```
<h5>⑤
```sh
unzip 1.zip && rm 1.zip
```
<h5>⑥
```sh
mv BaiduPCS-Go-v3.5.6-android-21-arm64 BaiduPCS-Go
```
<h5>⑦
```sh
cd ~/BaiduPCS-Go && ./BaiduPCS-Go
```
<h5>⑧
```sh
config set -savedir /sdcard/download
```
<h5>⑨
```sh
login
```

**输入百度网盘账号（用户名/手机号/邮箱）
然后，输入密码
——由于密码为输入不可见，需事先复制到剪贴板，此时再粘贴。
接着，有的可能需要验证，输入验证码，回车，即可。
现在，配置结束，可以下载了**
