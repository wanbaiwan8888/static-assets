# TVBox 纯成人接口配置

更新: 2026/11/24 14:13:53

## 地址

- 全量（14 个不重复片库）: `https://raw.githubusercontent.com/wanbaiwan8888/tvbox18/main/18plus-full.json`
- jsDelivr（走 CDN，更快）: `https://cdn.jsdelivr.net/gh/wanbaiwan8888/tvbox18@main/18plus-full.json`
- 网盘类（AList 自建，需 jar）: `https://raw.githubusercontent.com/wanbaiwan8888/tvbox18/main/18plus-pan.json`

## 说明

- 全部源为第三方公开 CMS，`type 0`=XML / `type 1`=JSON，**无需 jar**；配置本身放在本仓库，与本机无关。
- 片库已按「总条数+首条片名」去重，镜像域名只保留最快一个。
- 网盘类没有现成公网成人源：色花堂/pg.jar 等公开 jar 已 403/超时，唯一可行是自建 AList 后把目录挂上。
- 域名会失效，定期跑 `node _verify18.mjs` 复测。