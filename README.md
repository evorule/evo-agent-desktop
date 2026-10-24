# evo-agent-desktop

evo-agent 桌面壳（Windows x64）的二进制发布与自动更新仓。

- 安装包（NSIS）、更新签名与更新清单随 Release 发布；桌面壳内置更新通道按 `latest` 标签拉取 `latest.json` 完成自动升级
- 源代码与产品文档见主仓：https://github.com/evorule/evo-agent （Gitee 镜像：https://gitee.com/evorule/evo-agent ）
- 安装包含 AGPL-3.0-or-later 产物，随主仓协议分发

## 快速上手（两步开始用）

> 全程只有两个动作：**装上，贴一把密钥**。

**第 1 步 · 下载安装**：到 [Releases 最新版](https://github.com/evorule/evo-agent-desktop/releases/latest) 下载名字带 `_setup.exe` 的文件，双击安装（国内下载慢可走 [Gitee 同页](https://gitee.com/evorule/evo-agent-desktop/releases)）。若 Windows 提示「已保护你的电脑」：点 **更多信息 → 仍要运行**（安装包暂无代码签名，正常现象）。

**第 2 步 · 贴一把模型密钥**：首次启动的向导里，粘贴你自己的 MiniMax API Key（到 [platform.minimaxi.com](https://platform.minimaxi.com) 注册 → 控制台「接口密钥」→ 新建并复制）。密钥加密保存在你自己电脑上，只用于连接你选的模型服务。

完成。桌面图标双击即用；软件自动保持更新；对话与数据全程留在本机。

### 常见问题

| 现象 | 处理 |
|---|---|
| 杀毒软件报警或删安装包 | 无代码签名所致，将文件加入信任/白名单即可 |
| 如何升级 | 应用内自动更新（双通道），无需手动下载 |
| 我的数据在哪 | 全部在本机安装目录，不经任何服务器 |
| 如何卸载 | 系统「设置 → 应用」标准卸载 |

---

## 维护者信息（发布与更新通道）

### 更新通道

| 端点 | 形态 |
|------|------|
| Gitee（主） | `https://gitee.com/evorule/evo-agent-desktop/releases/download/latest/latest.json` |
| GitHub（备） | `https://github.com/evorule/evo-agent-desktop/releases/latest/download/latest.json` |

发布流程：构建机产出三件套（setup.exe / .sig / latest.json）→ 维护 `latest` 标签 Release 附件。