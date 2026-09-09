# Knowken 1.6.0

**看清你的 Codex Token 用量。**

Knowken 是一款本地用量应用，按日期、模型、项目和任务整理 Codex 已记录的 Token 使用情况。开发者：**Sense**。

## 功能

- 每日趋势、模型分布、项目统计与任务明细。
- 日期、模型、项目、时区筛选、任务搜索和子代理合并。
- 任务小时用量时间线，可展开查看模型及主／子会话来源。
- 本周／本月与上期同期比较。
- 当前筛选范围的 CSV 导出与默认匿名分享 PNG。
- 每日／每周 Token 目标和 80%／100% 页面提醒。
- 简体中文、English、日本語；中文支持万 / 亿或 K / M / B，英文和日语使用 K / M / B。
- 深色、浅色或跟随系统外观，字号、次要文字深浅和主题色可调。
- 重启可恢复的持久统计缓存与稳定性保护。

## 下载与运行

从 [Releases](https://github.com/Sense-Uesugi/Knowken/releases) 下载对应平台的压缩包。

Windows x64：完整解压到当前用户可写的目录后双击 **Knowken.exe**。退出时使用 **Stop-Knowken.cmd** 或 **停止 Knowken.vbs**。

GNU/Linux x64：将 `.tar.gz` 完整解压到可写且允许执行的目录后，执行 `./Knowken`。需要时可使用 `./Knowken --no-browser`，终端会显示访问地址；停止服务执行 `./Knowken --stop`。

Linux 运行时需要 kernel ≥ 4.18、glibc ≥ 2.28、GLIBCXX ≥ 3.4.25。提供 GNU/Linux x64 包，不提供 ARM 或 musl 包；需要可用的 `/proc` 和现代浏览器；桌面自动打开使用可选的 `xdg-open`。无需另行安装运行时。

本版未签名。Windows 已在本机隔离验收；Linux 已在 WSL2 中的 Ubuntu 24.04.3 验收，浏览器检查使用 Windows Edge 连接 Linux 服务。其他发行版、最低兼容边界和 Linux 桌面自动打开尚未实测。

## 本地与隐私

应用只读当前电脑的 Codex 日志，不上传对话或用量数据，不跨设备同步记录。统计基于现存日志，可能不完整，不等同于官方账单、费用或账号额度。

公开仓库只提供产品材料与许可，二进制通过 Releases 提供，源码不公开。
