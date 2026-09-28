

```bash
bash <(curl -fsSL https://raw.githubusercontent.com/chenlee86/tytysteria/refs/heads/main/server/ty.sh)
```

安装后可直接用 `hihy` 命令唤起菜单。

## 多配置版 ty2.sh

同一台机器需要同时跑多个配置（不同端口/证书/参数）时使用：

```bash
bash <(curl -fsSL https://raw.githubusercontent.com/chenlee86/tytysteria/refs/heads/main/server/ty2.sh)
```

- 菜单 17/18/19：查看所有配置、切换当前配置、新增一个配置
- 命令行指定配置：`hihy -i <名称> [命令]`，例如 `hihy -i b restart`；`hihy instances` 列出所有配置
- 默认配置与 ty.sh 路径完全一致，已有安装可直接用 ty2.sh 接管；新增配置 `b` 使用 `/etc/hihy-b`、服务 `hihy-b`
- 卸载只删除当前配置，其他配置还在时保留 `hihy` 命令等共享组件

