# Loon Rules

## 合并后的规则订阅

以下链接可直接添加到 Loon：

| 规则 | 订阅链接 |
|---|---|
| Apple | [Apple.list](https://raw.githubusercontent.com/Cola201118/Loon/main/rules/Apple.list) |
| China | [China.list](https://raw.githubusercontent.com/Cola201118/Loon/main/rules/China.list) |
| Proxy | [Proxy.list](https://raw.githubusercontent.com/Cola201118/Loon/main/rules/Proxy.list) |

## AI 合并订阅

| 规则 | 订阅链接 |
|---|---|
| AI（OpenAI + Gemini + Muse） | [AI.list](https://raw.githubusercontent.com/Cola201118/Loon/main/rules/AI.list) |

上游来源：`poohyeban/loon-rules` 的 `OpenAI/OpenAI-NoResolve.list` 与 `VPSDance/ai-proxy-rules` 的 `rules/loon/google-ai.list`。仓库会随现有 GitHub Actions 每 6 小时检查并同步，合并时按规则内容去重，保留 OpenAI IP 规则的 `no-resolve`。AI.list 还包含 Muse 的 13 条上游规则（随 Gemini 上游带入，同步后仍在）和 6 条手动补充规则；手动补充的 6 条同时保存在独立的 `rules/Muse-manual.list` 中，同步只按 OpenAI + Gemini 重新生成 AI.list，下次同步会丢掉这 6 条，如需长期保留请同时订阅 Muse-manual.list。

## 独立 AI 服务订阅

| 规则 | 订阅链接 | 当前规则数 |
|---|---|---:|
| Muse（Meta AI / Muse / Llama / SAM 分类） | [Muse.list](https://raw.githubusercontent.com/Cola201118/Loon/main/rules/Muse.list) | 19 |
| Muse 手动补充（同步不会覆盖） | [Muse-manual.list](https://raw.githubusercontent.com/Cola201118/Loon/main/rules/Muse-manual.list) | 6 |
| Grok（xAI / Grok / Grokipedia 分类） | [Grok.list](https://raw.githubusercontent.com/Cola201118/Loon/main/rules/Grok.list) | 5 |

Muse 与 Grok 的上游规则也包含在 AI.list 中，仍保留独立订阅文件；两份独立文件不与 OpenAI、Gemini 或彼此合并。上游采用 YUDIDIFEI/Scripts 的 Loon AI 分类清单；GitHub Actions 每 6 小时同步并按分类提取。Muse 分类按上游原始分组，包含 Meta AI、Muse、Llama 与 SAM 相关域名。Muse.list 目前为上游 13 条加手动补充 6 条，共 19 条；手动补充的 6 条同时保存在独立的 rules/Muse-manual.list 中，同步只重写 Muse.list，不会覆盖该文件，Loon 里请同时订阅两份，同步后 Muse.list 会回到 13 条，手动补充仍由 Muse-manual.list 提供。

## 上游规则来源

### Apple

| 来源 | 上游链接 |
|---|---|
| Siri | [Siri-Direct.list](https://raw.githubusercontent.com/Kianuni/AppleFlow/main/rules/surge/Siri-Direct.list) |
| Apple APNs | [Apple-APNs-Direct.list](https://raw.githubusercontent.com/Kianuni/AppleFlow/main/rules/surge/Apple-APNs-Direct.list) |
| Apple | [Apple-Direct.lsr](https://raw.githubusercontent.com/o-ocn/loon-rules/main/dist/Apple-Direct.lsr) |

### China

| 来源 | 上游链接 |
|---|---|
| ChinaMax | [ChinaMax.list](https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Loon/ChinaMax/ChinaMax.list) |
| ChinaMax Domain | [ChinaMax_Domain.list](https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Loon/ChinaMax/ChinaMax_Domain.list) |
| China ASN | [ChinaASN.list](https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Loon/ChinaASN/ChinaASN.list) |
| LAN | [Lan.list](https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Loon/Lan/Lan.list) |

### Proxy

| 本地镜像文件 | 上游链接 |
|---|---|
| Proxy source | [Proxy.list](https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Loon/Proxy/Proxy.list) |
| Proxy Domain | [Proxy_Domain.list](https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Loon/Proxy/Proxy_Domain.list) |
| GitHub | [GitHub.list](https://raw.githubusercontent.com/Cola201118/Loon/main/rules/GitHub.list) | [GitHub.list](https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Loon/GitHub/GitHub.list) |
| Google | [Google.list](https://raw.githubusercontent.com/Cola201118/Loon/main/rules/Google.list) | [Google.list](https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Loon/Google/Google.list) |
| Telegram | [Telegram.list](https://raw.githubusercontent.com/Cola201118/Loon/main/rules/Telegram.list) | [Telegram.list](https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Loon/Telegram/Telegram.list) |
| Instagram | [Instagram.list](https://raw.githubusercontent.com/Cola201118/Loon/main/rules/Instagram.list) | [Instagram.list](https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Loon/Instagram/Instagram.list) |
| X (Twitter) | [Twitter.list](https://raw.githubusercontent.com/Cola201118/Loon/main/rules/Twitter.list) | [Twitter.list](https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Loon/Twitter/Twitter.list) |

仓库通过 GitHub Actions 定期同步上游规则，并生成合并订阅。Proxy 合并订阅为 `rules/Proxy.list`，包含通用 Proxy 规则及 GitHub、Google、Telegram、Instagram、X（Twitter）五组 App 规则。上游原文件分别保存在 `rules/Proxy_Source.list`、`rules/Proxy_Domain.list`、`rules/GitHub.list`、`rules/Google.list`、`rules/Telegram.list`、`rules/Instagram.list` 和 `rules/Twitter.list`。生成时按规则类型和值去重。

## 感谢

感谢以下项目作者及维护者的规则整理与持续维护：

- [Kianuni / AppleFlow](https://github.com/Kianuni/AppleFlow)
- [o-ocn / loon-rules](https://github.com/o-ocn/loon-rules)
- [blackmatrix7 / ios_rule_script](https://github.com/blackmatrix7/ios_rule_script)
