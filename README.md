# tytysteria (hihy)

一键 **Hysteria2** 服务端管理脚本。本仓库是 [emptysuns/Hi_Hysteria](https://github.com/emptysuns/Hi_Hysteria)(原作者已删库)的可用重建版本 —— 修复了失效的自更新与 i18n 语言文件下载源,默认中文。

## 安装 / 运行

```bash
bash <(curl -fsSL https://raw.githubusercontent.com/chenlee86/tytysteria/refs/heads/main/server/ty.sh)
```

安装后可直接用 `hihy` 命令唤起菜单。

## 菜单功能

| # | 功能 | # | 功能 |
|---|---|---|---|
| 1 | 安装 Hysteria2(交互向导) | 9 | 重新配置 |
| 16 | 自动安装(一键) | 10 | 切换 IPv4/IPv6 优先 |
| 2 | 卸载 | 12 | 域名分流 / ACL |
| 3 / 4 / 5 | 启动 / 停止 / 重启 | 15 | Socks5 出站 |
| 6 | 运行状态 | 7 | 更新内核 |
| 8 | 查看客户端配置(二维码 / mihomo / sing-box) | 11 | 更新 hihy 脚本 |
| 13 | 流量统计 | 14 | 实时日志 |

## 结构

- `server/ty.sh` —— 主脚本(自更新 + 首启会从本仓库拉取)
- `server/i18n/{zh,en}.json` —— 界面文案(schema_version=1)

## 语言

默认 `zh`。用 `HIHY_LANG=en hihy` 可切换英文;持久化配置在 `/etc/hihy/conf/i18n.conf`。

## 依赖来源(均为存活的上游)

Hysteria 内核 `apernet/hysteria`、`yq` `mikefarah/yq`、分流规则 `Loyalsoldier/clash-rules`、WARP `fscarmen`;ECH 密钥本地生成。
