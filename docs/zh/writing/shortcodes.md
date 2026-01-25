# 短代码 (Shortcodes)

Stack 附带了一组您可以在内容中使用的 [短代码 (shortcodes)](https://gohugo.io/content-management/shortcodes/)。

本页面仅包含 Stack 特有的短代码。Hugo 内置的短代码在 [此处](https://gohugo.io/content-management/shortcodes/#use-hugos-built-in-shortcodes) 有文档说明。

## 哔哩哔哩视频 (Bilibili video)

嵌入 [哔哩哔哩 (Bilibili)](https://www.bilibili.com/) 视频。

```markdown
{{< bilibili VIDEO_ID PART_NUMBER >}}
```

`Video_ID` 可以在视频的 URL 中找到。例如，`https://www.bilibili.com/video/av12345678` 的视频 ID 是 `av12345678`。支持 `AV` 和 `BV` 格式。

`PART_NUMBER` 是可选的。它可用于指定要播放的视频分集。例如，`https://www.bilibili.com/video/av12345678?p=2` 的分集编号是 `2`。

## 腾讯视频 (Tencent video)

嵌入 [腾讯视频 (Tencent Video)](https://v.qq.com/) 视频。

```markdown
{{< tencent VIDEO_ID >}}
```

`Video_ID` 可以在视频的 URL 中找到。例如，`https://v.qq.com/x/cover/hzgtnf6tbvfekfv/g0014r3khdw.html` 的视频 ID 是 `g0014r3khdw`。

## YouTube 视频

嵌入 [YouTube](https://www.youtube.com/) 视频。

```markdown
{{< youtube VIDEO_ID >}}
```

`Video_ID` 可以在视频的 URL 中找到。例如，`https://www.youtube.com/watch?v=VIDEO_ID` 的视频 ID 是 `VIDEO_ID`。

## 通用视频文件

嵌入一个视频文件。

```markdown
{{< video VIDEO_URL >}}

{{< video src="VIDEO_URL" autoplay="true" poster="./video-poster.png" >}}
```

`VIDEO_URL` 可以是 URL 或相对于 `static` 目录的路径。例如，`src="/video/my-video.mp4"` 将嵌入站点文件夹中的 `static/video/my-video.mp4` 视频文件。

`autoplay` 属性是可选的。它可用于指定是否自动播放视频。`poster` 属性是可选的。它可用于指定视频的封面图片。

## GitLab

嵌入 [GitLab](https://gitlab.com/) 代码片段 (snippets)。

```markdown
{{< gitlab SNIPPET_ID >}}
```

`SNIPPET_ID` 可以在代码片段的 URL 中找到。例如，`https://gitlab.com/-/snippets/1234567` 的代码片段 ID 是 `1234567`。

## 引用 (Quote)

```markdown
{{< quote author="一位名人" source="他们写的书" url="https://zh.wikipedia.org/wiki/Book">}}
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
{{< /quote >}}
```