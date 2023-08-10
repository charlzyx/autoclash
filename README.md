[TOC]

# AutoClash

# 项目介绍

这是一个整合了 clash-for-linx 和 tcclash 的脚本

能够自动下载订阅文件, 并下载(如果不存在)启动 tpclash

## [clash-for-linux](https://github.com/wanhebin/clash-for-linux)

> 此项目是通过使用开源项目 clash 作为核心程序，再结合脚本实现简单的代理功能。

## [tpclash](https://github.com/mritd/tpclash)

> 这是一个用于 Clash Premium 的透明代理辅助工具, 由于众所周知周知的原因(手笨)而创建的.

# 如何使用

```sh
cd /etc/autoclash
git clone https://github.com/charlzyx/autoclash.git .
chmod +x autoclash.sh
./autoclash.sh [你的订阅地址]
```

需要自定义模版的话请修改 /temp/template_config.yaml 部分

# AutoClash 做了什么

1. 根据订阅地址下载并转换为合法的 clash config.yaml, 写入 /etc/clash.yaml
2. 检测 tpclash 服务是否存在, 不存在则进行下载与安装
3. 重启 tpclash 服务

## [TPClash 做了什么](https://github.com/mritd/tpclash#%E4%BA%94tpclash-%E5%81%9A%E4%BA%86%E4%BB%80%E4%B9%88)

> TPClash 在启动后会进行如下动作:
> 1、创建 /data/clash 目录(可自行指定成其他目录), 并将其作为 Clash 的 Home Dir
> 2、将 Clash 二进制文件、Dashboard(官方+yacd)、必要的 ruleset、Country.mmdb 释放到 /data/clash 目录
> 3、从本地或远程读取配置, 进行模版解析后复制到 /data/clash/xclash.yaml
> 4、启动官方的 Clash, 并设置必要参数, 比如 -ext-ui、-d 等
> 5、选择性进行网络配置, 例如为 Docker 用户自动设置 nftables
> 6、在后台持续监视本地或远程配置文件变动, 然后自动重载

## 如果你恰巧跟我一样实在 Proxmox VE 里面搭建软路由使用的话

可以看看我的笔记 [charlzyx.github.io/boom](https://charlzyx.github.io/boom/)
