# 文章

文章页面的配置。

`[Params.Article]` 下的字段。

## headingAnchor

- 类型：`bool`
- 默认值：`false`

启用标题旁边的 # 锚点链接，仅在悬停时可见。

## math

- 类型：`bool`

通过 [KaTeX](https://katex.org/) 启用数学公式支持。可以被 Front Matter 字段 `math` 覆盖。

## toc

- 类型：`bool`

默认启用文章目录。可以被 Front Matter 字段 `toc` 覆盖。

::: warning
您仍需要将 [`toc` 小部件](widgets.md#toc) 添加到侧边栏以显示目录。
::: 


## readingTime

- 类型：`bool`
- 默认值：`true`

显示文章的预计阅读时间。

## license

- 类型：`map[string]:(bool|string)`

与许可证相关的配置。

### license.enabled

- 类型：`bool`
- 默认值：`false`

在文章下方显示许可证信息。

### license.default

- 类型：`string`
- 默认值：`Licensed under CC BY-NC-SA 4.0`

文章下方显示的默认许可证文本。可以被 Front Matter 字段 `license` 覆盖。
