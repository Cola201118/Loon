# Loon Apple Rules

This repository mirrors three upstream Apple-related rule files and also provides one combined subscription file.

## One-link subscription

Subscribe to this single file in Loon:

`https://raw.githubusercontent.com/Cola201118/Loon/main/rules/Apple-Combined.list`

## Individual source files

| Local file | Upstream source |
|---|---|
| `rules/Siri-Direct.list` | https://raw.githubusercontent.com/Kianuni/AppleFlow/main/rules/surge/Siri-Direct.list |
| `rules/Apple-APNs-Direct.list` | https://raw.githubusercontent.com/Kianuni/AppleFlow/main/rules/surge/Apple-APNs-Direct.list |
| `rules/Apple-Direct.lsr` | https://raw.githubusercontent.com/o-ocn/loon-rules/main/dist/Apple-Direct.lsr |

GitHub Actions checks the three upstream files every 6 hours, regenerates `rules/Apple-Combined.list`, and commits changes only when needed. It can also be run manually from the Actions tab.
