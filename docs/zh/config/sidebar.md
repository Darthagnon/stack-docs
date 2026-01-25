# 侧边栏

与左侧侧边栏相关的设置。

字段位于 `[Params.Sidebar]` 部分。

## compact

- 类型：`bool`
- 默认值：`false`

启用侧边栏的紧凑版本。

## emoji

- 类型：`string`

显示在头像上方的 Emoji。

## subtitle

- 类型：`string`

显示在站点标题下方的副标题。

## avatar

- 类型：`map[string]:(bool|string)`

与头像相关的配置。

### avatar.enabled

- 类型：`bool`
- 默认值：`true`

启用头像。

### avatar.src

- 类型：`string`
- 默认值：`img/avatar.png`

头像图片的路径。

### avatar.local

- 类型：`bool`
- 默认值：`true`

如果为 `true`，则头像图片应放置在 `assets/${avatar.src}` 下，这允许主题自动调整图片大小。
