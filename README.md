# Quantumult X 自用配置

自用 Quantumult X 配置文件，提供三个版本满足不同需求。

## 分流规则

所有分流规则均来自 [szkane/ClashRuleSet](https://github.com/szkane/ClashRuleSet)，通过 `opt-parser=true` 由 Quantumult X 资源解析器自动转换 Clash 格式规则。

## 版本说明

### Full（完整版）— `QuantumultX-ViaVxxx-Full.conf`

功能最全的版本，适合需要精细化分流和解锁功能的用户。

- **策略组**：16 组（含 AI 服务、电报代理、港台番剧、国际媒体等细分组）
- **分流规则**：27 条（覆盖广告拦截、隐私保护、AI 服务、加密货币、开发者工具、学术资源、Discord、GitHub、YouTube、Spotify 等）
- **Rewrite**：23 条（去广告 + iRingo 增强 + Bilibili/DualSubs + TikTok 解锁 + Leica Pro/Pandora/Tutu/Lightroom 解锁）
- **脚本任务**：流媒体解锁查询、60s 新闻

### Standard（标准版）— `QuantumultX-ViaVxxx-Standard.conf`

平衡版本，保留核心分流和增强功能，去掉细分规则和 App 解锁脚本。

- **策略组**：16 组（与完整版相同）
- **分流规则**：15 条（保留核心分流，去掉 Crypto、Scholar、Edutools、Discord、Web3、CiciAI、Perplexity、GitHub、YouTube、Spotify、LocalAreaNetwork 等细分规则）
- **Rewrite**：19 条（去广告 + iRingo 增强 + Bilibili/DualSubs + TikTok 解锁，**不含** Leica Pro/Pandora/Tutu/Lightroom 解锁）
- **脚本任务**：流媒体解锁查询、60s 新闻

### Lite（精简版）— `QuantumultX-ViaVxxx-Lite.conf`

极简版本，适合只需基础代理和去广告的用户。

- **策略组**：8 组（仅保留 Main Policy、低倍率、全球加速、苹果服务、黑白名单、特殊节点及地区节点）
- **分流规则**：8 条（直连修正、广告拦截、隐私保护、谷歌服务、全球加速、苹果服务、国内网站、国内公司 IP）
- **Rewrite**：4 条（YouTube 去广告、神机去广告、贴吧去广告、咸鱼净化）
- **脚本任务**：无

## 版本对比

| 功能                                   | Lite | Standard | Full |
| ------------------------------------ |:----:|:--------:|:----:|
| 策略组数量                                | 8    | 16       | 16   |
| 分流规则数量                               | 8    | 15       | 27   |
| Rewrite 数量                           | 4    | 19       | 23   |
| 广告拦截                                 | ✅    | ✅        | ✅    |
| iRingo 增强                            | ❌    | ✅        | ✅    |
| Bilibili 增强/去广告                      | ❌    | ✅        | ✅    |
| DualSubs 双语字幕                        | ❌    | ✅        | ✅    |
| TikTok 解锁                            | ❌    | ✅        | ✅    |
| AI 服务分流                              | ❌    | ✅        | ✅    |
| 电报专用代理                               | ❌    | ✅        | ✅    |
| 细分规则（Crypto/Scholar/Discord 等）       | ❌    | ❌        | ✅    |
| App 解锁（Leica/Pandora/Tutu/Lightroom） | ❌    | ❌        | ✅    |
| 脚本任务                                 | ❌    | ✅        | ✅    |

## 使用方法

1. 下载对应版本的 `.conf` 文件
2. 在 Quantumult X 中导入配置
3. 根据需要修改 `[server_remote]` 中的订阅链接

## 致谢

- 分流规则：[szkane/ClashRuleSet](https://github.com/szkane/ClashRuleSet)
- iRingo 增强：[NSRingo](https://nsringo.github.io/)
- Bilibili 增强/去广告：[BiliUniverse](https://biliuniverse.io/)
- DualSubs 双语字幕：[DualSubs](https://dualsubs.github.io/)
- App 解锁脚本：[yfamilys](https://yfamilys.com/quantumultx)
- 资源解析器：[KOP-XIAO/QuantumultX](https://github.com/KOP-XIAO/QuantumultX)
- 策略组图标：[Orz-3/mini](https://github.com/Orz-3/mini)
