# 配色方案

此主题提供浅色和深色配色方案。

字段位于 `[Params.colorScheme]` 部分。

## toggle

- 类型：`bool`
- 默认值：`true`

显示配色方案切换按钮。

如果设置为 `false`，配色方案将由 `default` 选项决定。

## default

- 类型：`string (light|dark|auto)`
- 默认值：`auto`

默认配色方案，在 `toggle` 选项设置为 `false` 或用户首次访问站点时使用。

设置为 `auto` 时，配色方案将由用户的系统偏好决定（`prefers-color-scheme` 媒体查询）。
