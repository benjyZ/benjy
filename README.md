# benjy

Clash / OpenClash 分流配置与订阅转换模板仓库。

## 文件说明

### Sub-Store / 订阅转换模板（放根目录）

| 文件 | 说明 |
| --- | --- |
| `AG of FL.ini` | 精简版转换模板：AI、GitHub、TikTok、Telegram、流媒体、国外/国内分组 |
| `Clash-Full of AG.ini` | 完整版转换模板：AI、社交、游戏、流媒体、电商等全分组 |
| `FL.ini` | OpenClash 转换模板（Aethersailor 风格，含谷歌 FCM、小米服务、国内媒体等） |

### 可直接使用的 Clash 配置（`proxy/` 目录）

| 文件 | 说明 |
| --- | --- |
| `proxy/clash-all-fallback of AG.yaml` | 完整 Clash 配置，含 fallback 策略组（需自行填写机场订阅地址） |
| `proxy/clash-all-globe of AG.ini` | Sub-Store 转换模板（带图标分组） |
| `proxy/New openclash of AG.ini` | Sub-Store 转换模板（OpenClash 用，无图标版） |

### 其他

| 文件 | 说明 |
| --- | --- |
| `worker.js` | 自部署订阅转换后端（psub 项目构建产物，部署到 Cloudflare Worker 使用） |

## 上游规则源

模板引用的分流规则全部来自以下公开仓库（自动跟随上游更新）：

- [blackmatrix7/ios_rule_script](https://github.com/blackmatrix7/ios_rule_script) — 主力规则集
- [liandu2024/clash](https://github.com/liandu2024/clash) — AI / 代理规则
- [Aethersailor/Custom_OpenClash_Rules](https://github.com/Aethersailor/Custom_OpenClash_Rules) — OpenClash 自定义规则
- [ACL4SSR/ACL4SSR](https://github.com/ACL4SSR/ACL4SSR) — 国内/国外基础规则
- [MetaCubeX/meta-rules-dat](https://github.com/MetaCubeX/meta-rules-dat) — geosite / geoip 二进制规则
- [bulianglin/psub](https://github.com/bulianglin/psub) — worker.js 的上游源码

## 维护记录

- **2026-10-06**：修复 4 个失效的规则链接（liandu2024 的 `AI/AI2/Proxy.list` 已迁移到 `list/` 目录；Aethersailor 的 `Ozon.list` 已下架删除）；替换已失效的 `github.moeyy.xyz` 代理前缀为直连地址；删除与 `New openclash of AG.ini` 内容完全重复的 `proxy/clash-all-globe-noicon of AG.ini`；新增本 README。
