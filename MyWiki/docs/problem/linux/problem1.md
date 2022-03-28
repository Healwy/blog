
# Ubuntu 18.04 卸载python3后进不去图形界面解决方法

## 1. 确保网络连接正常
```
$ ip addr
$ nmcli
$ ping www.baidu.com
```
如果网络连接不上可以使用安卓手机进行usb网络共享，并配置动态ip
```
$ sudo dhclient
```

## 2. 设置apt源并更新
```
$ vi /etc/apt/source.list

```
```
deb http://mirrors.aliyun.com/ubuntu/ bionic main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ bionic-security main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ bionic-updates main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ bionic-backports main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ bionic-proposed main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ bionic main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ bionic-security main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ bionic-updates main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ bionic-backports main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ bionic-proposed main restricted universe multiverse
```
```
$ sudo apt-get update 
$ sudo apt-get install -f
```

## 3. 安装ubuntu 桌面软件

```
sudo apt-get install ubuntu-minimal ubuntu-standard ubuntu-desktop
```

## 4. 重启电脑
```
$ sudo reboot
```