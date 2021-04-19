## Features

MiniValine 自 version 6.x 起回归极简主义！ 因此 6.x 移除了 5.x 的全部功能特性，只保留了基础评论功能！！！

> Less is More
------------------------------

> 基于 CloudFlareWorker 和 CloudFlareKV/IPFS 技术的极简风评论系统

* 使用 Cloudflare Workers 构建无服务器应用程序并部署到Cloudflare的边缘网络
* 使用 Cloudflare Workers KV 全球分布式键值存储构建高度动态API
* 使用 IPFS 分布式文件系统实现去中心化分布式存储

# 参数和指标

- 前端 JS 脚本完整版共计一个（MiniValine.min.js） 文件大小约为 80 KB，gzip 压缩后约为 25 KB。
- 前端 JS 脚本无样式版共计一个（MiniValine.o.min.js） 文件大小约为 45 KB。
- 系统关键请求共计3个。
- ~~中国地区使用 CloudFlareAnycast 技术和 DNSPOD 智能解析技术 以及 优选 CloudFlare节点 IP 负载均衡的方法，~~ 系统关键请求时间可在 200-500ms 左右。
