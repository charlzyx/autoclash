[TOC]

# 项目介绍

> [上游项目参考](https://github.com/wanhebin/clash-for-linux)

## 不同

- start.sh -> dl.sh 只用来下载 -> /etc/clash/clash.yaml
- /temp/template_config.yaml 自己使用的配置

## 目的

配合 [tpclash](https://github.com/mritd/tpclash) 使用

# 全自动

```sh
git clone https://github.com/charlzyx/autoclash.git /etc/autoclash
chmod +x /etc/autoclash/autoclash.sh
ln -s /etc/autoclash/autoclash.sh /usr/local/bin/autoclash
```
