# TVBox 纯成人接口配置

更新: 2026/11/24 14:42:12

## 配置地址

| 用途 | 固定版本地址（推荐，缓存不会串） |
|---|---|
| **成人直连（14 个不重复片库）** | `https://cdn.jsdelivr.net/gh/wanbaiwan8888/tvbox18@v3/18plus-full.json` |
| **成人网盘搜索（12 站）** | `https://cdn.jsdelivr.net/gh/wanbaiwan8888/tvbox18@v3/18plus-pan.json` |

`@main` 也可用，但 jsDelivr 对分支有 12h 缓存，改完文件不刷；固定 tag 最稳。

## 网盘搜索怎么来的

- 公网现成的成人网盘接口已全部失效：色花堂 `sehuatang.net` 403、七陌 `fan.txt` 403、notabug `pg.jar` 404、`agit.ai` 跳转空页、`s3.tebi.io`/`liulili.1919810.com` 不可达、`pansearch.me` 不可达、jsDelivr 拒收 `.jar` 后缀。
- 现在用的是 `pg.jar`（3.74MB，含 DaPanSo/PanSearch/PanSou/Panta/YiSo/Panyq/MiaoSou/Qianfan/YunSo/UpYun/EightEight/Funletu 等网盘搜索类），以 `pg.txt` 自托管在 jsDelivr，md5 `1a1efb7d1e3ba4b56692d2f9859cc082`。
- 上游已实测有成人内容：`dapanso.com` 搜「麻豆」出 4 条夸克分享、「无码」9 条、「探花」6 条、「成人」15 条（`pan.quark.cn/s/...`）。

## 说明

- 直连那 14 个源是纯 m3u8，无需 jar，不依赖任何本机服务。
- 网盘搜索返回的是夸克/UC 分享链接，播放要登录对应网盘，非会员会被限速——这是网盘类的物理上限，不是接口慢。
- 搜索类站点常换域名，若某个源搜不出东西，换同配置里其它站；`_verify18.mjs` 可复测直连源。