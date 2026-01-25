# 自定义页眉 / 页脚

主题中预留了两个用于自定义 HTML 的空文件，这对于添加自定义脚本或样式表非常有用：

* `layouts/partials/head/custom.html`
* `layouts/partials/footer/custom.html`

要覆盖它们：

1. 在您的 Hugo 站点文件夹下创建 `layouts/partials/footer/custom.html`
2. 在该文件中插入自定义代码。

## 示例：为文章内容自定义字体系列

默认情况下，此主题使用 [Lato](https://fonts.google.com/specimen/Lato) 作为文章内容字体。此示例说明如何使用其他字体。例如，让我们将文章字体系列更改为 [Merriweather](https://fonts.google.com/specimen/Merriweather)。

在您的 Hugo 站点文件夹下创建 `layouts/partials/head/custom.html`，代码如下：

```html
<style>
    /* 覆盖 CSS 变量 */
    :root {
        --article-font-family: "Merriweather", var(--base-font-family);
    }
</style>

<script>
    (function () {
        const customFont = document.createElement('link');
        customFont.href = "https://fonts.googleapis.com/css2?family=Merriweather:wght@400;700&display=swap";
    
        customFont.type = "text/css";
        customFont.rel = "stylesheet";
    
        document.head.appendChild(customFont);
    }());
</script>
```
