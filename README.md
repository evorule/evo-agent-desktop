# evo-agent-desktop

Desktop shell for the evorule agent workstation (Windows x64): binary releases and auto-updates.

[![License: AGPL-3.0-or-later][badge-license]][license-link]

**License**: AGPL-3.0-or-later artifacts, distributed under the [main repo](https://github.com/evorule/evo-agent)'s licensing — source code and product docs live there.

## Prerequisites

- Windows (x64)
- The installer is not code-signed yet — expect a SmartScreen prompt on first install

## Install (two steps)

1. **Download & install** — grab the `_setup.exe` from the [latest release](https://github.com/evorule/evo-agent-desktop/releases/latest) and double-click it. If Windows says it protected your PC, choose **More info → Run anyway**.
2. **Paste a model key** — the first-launch wizard asks for your own MiniMax API key (register at [platform.minimaxi.com](https://platform.minimaxi.com) → console → API keys → create and copy). The key is stored encrypted on your own machine and is used only to connect to the model service you choose.

Done — double-click the desktop icon to start; the app keeps itself updated; conversations and data stay on your machine.

## Run & update

| Symptom | Fix |
|---|---|
| Antivirus flags or deletes the installer | caused by the missing code signature — whitelist the file |
| How do I upgrade | in-app auto-update (dual channel) — no manual download needed |
| Where is my data | all in the local install directory, never through a server |
| How do I uninstall | standard Windows "Settings → Apps" uninstall |

Auto-update fetches `latest.json` from the `latest` tag's release assets (installer, update signature, and update manifest ship with each release):

| Endpoint | URL |
|---|---|
| Gitee | `https://gitee.com/evorule/evo-agent-desktop/releases/download/latest/latest.json` |
| GitHub | `https://github.com/evorule/evo-agent-desktop/releases/latest/download/latest.json` |

> [!NOTE]
> Two independent channels serve the same manifest; the listing order mirrors the product's runtime configuration and is reworded whenever that configuration changes.

## License

AGPL-3.0-or-later — the installer ships artifacts licensed under the main repo's licensing ([evorule/evo-agent](https://github.com/evorule/evo-agent)). License documents: [LICENSE](LICENSE), [DUAL_LICENSE.md](DUAL_LICENSE.md), [FREE_COMMERCIAL_LICENSE.md](FREE_COMMERCIAL_LICENSE.md) (free waiver for eligible entities), [COMMERCIAL_LICENSE.md](COMMERCIAL_LICENSE.md), [NOTICE.md](NOTICE.md).

[badge-license]: https://img.shields.io/badge/license-AGPL--3.0--or--later-blue?style=flat-square
[license-link]: LICENSE
