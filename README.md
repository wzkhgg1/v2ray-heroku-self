# V2Ray Heroku
 原始作者：https://github.com/bclswl0827/v2ray-heroku
# 最近很多作者的优秀作品陆续转为私有甚至删库。个人认为比较有学习意义的项目就备份下来，留作学习。请勿其他用途
## 概述

用于在 Heroku 上部署 V2Ray Websocket。

**Heroku 为我们提供了免费的容器服务，我们不应该滥用它，所以本项目不宜做为长期翻墙使用。**

**可以部署两个以上的应用，实现 [负载均衡](https://toutyrater.github.io/app/balance.html)，避免长时间大流量连接某一应用而被 Heroku 判定为滥用。**

**Heroku 的网络并不稳定，部署前请三思。**

## 镜像

本镜像不会因为大量占用资源而被封号。

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://dashboard.heroku.com/new?template=https%3A%2F%2Fgithub.com%2Fwzkhgg1%2Fv2ray-heroku-self)

## ENV 设定

### UUID

`UUID` > `一个 UUID，供用户连接时验证身份使用`。

## 注意

WebSocket 路径为 `/`。

`alterId` 为 `64`。

V2Ray 将在部署时自动安装最新版本。

**出于安全考量，除非使用 CDN，否则请不要使用自定义域名，而使用 Heroku 分配的二级域名，以实现 V2Ray Websocket + TLS。**
