# 图片处理

此主题使用 Hugo 内置的图片处理功能来调整大小和优化本地图片（使用页面包功能包含的图片）。这在您构建站点时自动完成。

如果您的站点中有很多图片，这可能会减慢构建过程。您可以在这里选择禁用此功能。

## cover

- 类型：`map[string]bool`

### cover.enabled

- 类型：`bool`
- 默认值：`true`

为封面（特色）图片启用图片处理。

## content

- 类型：`map[string]bool`

### content.enabled

- 类型：`bool`
- 默认值：`true`

为内容中的图片启用图片处理。