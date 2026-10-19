# evo-agent-desktop

evo-agent 桌面壳（Windows x64）的二进制发布与自动更新仓。

- 安装包（NSIS）、更新签名与更新清单随 Release 发布；桌面壳内置更新通道按 `latest` 标签拉取 `latest.json` 完成自动升级
- 源代码与产品文档见主仓：https://github.com/evorule/evo-agent （Gitee 镜像：https://gitee.com/evorule/evo-agent ）
- 安装包含 AGPL-3.0-or-later 产物，随主仓协议分发

## 更新通道

| 端点 | 形态 |
|------|------|
| Gitee（主） | `https://gitee.com/evorule/evo-agent-desktop/releases/download/latest/latest.json` |
| GitHub（备） | `https://github.com/evorule/evo-agent-desktop/releases/latest/download/latest.json` |

发布流程：构建机产出三件套（setup.exe / .sig / latest.json）→ 维护 `latest` 标签 Release 附件。