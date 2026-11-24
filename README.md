# TVBox 纯成人接口配置

更新: 2026/11/24 14:21:26

## 配置地址（直接粘进 TVBox / 影视仓）

| 用途 | 地址 |
|---|---|
| **全量（14 个不重复片库）** | `https://cdn.jsdelivr.net/gh/wanbaiwan8888/tvbox18@main/18plus-full.json` |
| 网盘类（AList 自建） | `https://cdn.jsdelivr.net/gh/wanbaiwan8888/tvbox18@main/18plus-pan.json` |

备用 CDN（jsDelivr 主域抽风时换）:

- `https://fastly.jsdelivr.net/gh/wanbaiwan8888/tvbox18@main/18plus-full.json`
- `https://gcore.jsdelivr.net/gh/wanbaiwan8888/tvbox18@main/18plus-full.json`

## 说明

- 全部源为第三方公开 CMS，`type 0`=XML / `type 1`=JSON，**无需 jar**；配置托管在 jsDelivr，家里那台 192.168.110.16 关机也能用。
- 片库已按「总条数+首条片名」去重，镜像域名只保留最快的那个。
- 网盘类那条需要 jar：本仓 `fish.txt` 就是 jar 本体（jsDelivr 不给 `.jar` 后缀，改 `.txt` 一样加载，只看 md5 `d07d678a0f3b813b67826a492b297581`）。
- 网盘源的 `ext.drives[0].server` 要改成你自己的 AList（默认占位 `http://127.0.0.1:5244/`，密码 `REPLACE_ALIST_PWD`）。
- 公开成人网盘源已全部失效（色花堂/pg.jar/pansearch 均 403 或不可达），所以这一条只做「自建目录」入口。
- `fish.jar` 是同一份二进制（留给需要 `.jar` 后缀的播放器）；`fish.txt` 用于 jsDelivr。

## 复测

域名会失效。用仓库里的 `_verify18.mjs` 定期复跑：`ac=list`×3 取中位 + `ac=detail` + m3u8 + 首个 ts 分片。