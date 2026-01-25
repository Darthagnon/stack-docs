# 默认图片

默认图片是在末设置特色图片时，页面将使用的图片。这对于 Open Graph 和 Twitter 卡片非常有用。

## opengraph

Open Graph 和 Twitter 的默认图片。

### opengraph.enabled

- 类型：`bool`
- 默认值：`false`

启用 Open Graph 和 Twitter 的默认图片。

### opengraph.src

- 类型：`string`

图片文件的路径。

### opengraph.local

- 类型：`bool`
- 默认值：`false`

如果为 `true`，则图片为本地文件，且必须放置在 `assets` 文件夹下。否则，它是一个远程 URL。

例如，如果 `src` 设置为 `img/default.jpg`，则图片文件必须放置在 `assets/img/default.jpg` 下。