# Loon Rules

This repository mirrors upstream Apple-related rule files and China-related rule sources, and provides generated subscription files.

## Apple subscription

Subscribe to:

`https://raw.githubusercontent.com/Cola201118/Loon/main/rules/Apple.list`

## Individual Apple source files

| Local file | Upstream source |
|---|---|
| `rules/Siri.list` | https://raw.githubusercontent.com/Kianuni/AppleFlow/main/rules/surge/Siri-Direct.list |
| `rules/Apple-APNs.list` | https://raw.githubusercontent.com/Kianuni/AppleFlow/main/rules/surge/Apple-APNs-Direct.list |
| `rules/Apple.lsr` | https://raw.githubusercontent.com/o-ocn/loon-rules/main/dist/Apple-Direct.lsr |

GitHub Actions checks the three upstream Apple files every 6 hours, regenerates `rules/Apple.list`, and commits changes only when needed.

## China rule sources

The China source files are kept separately under `rules/`; the generated subscription is `rules/China.list`.
