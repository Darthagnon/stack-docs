# Open Graph

Open Graph 协议允许任何网页成为社交图谱中的富对象。

有关更多信息，请参见 [Open Graph 协议](http://ogp.me/)。

字段位于 `[Params.opengraph]` 部分。

## twitter

- 类型：`map[string]string`

可用字段：

### site

- 类型：`string`

站点的 Twitter 账号名称（不带 `@`）。

### card

- 类型：`string`

[Twitter 卡片类型](https://developer.twitter.com/en/docs/twitter-for-websites/cards/overview/abouts-cards)。可用值：`summary`、`summary_large_image`。
