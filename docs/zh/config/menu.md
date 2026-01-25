# 自定义菜单

主题中有两个菜单：主菜单 (`menu.main`) 和社交菜单 (`menu.social`，仅图标)。它们的配置方式类似。

## 第一种方法 (推荐)
如果您要添加的菜单项是一个页面，请在其 Front Matter 中添加 `menu` 字段：

```yaml
menu: 
    main:
        name: title (可选)
        weight: -90
        params:
            icon: icon-name
```

## 第二种方法

::: warning
不推荐使用此方法，因为主题无法检测当前页面是否在菜单中，且该菜单项不会被高亮显示。
:::

如果您要添加的菜单项不是一个页面，可以将其添加到配置文件中的 menu 部分：

TOML 示例：

```toml
[menu]
[[menu.main]]
    name = "Home"
    url = "/"
    weight = 10
    identifier = "home"
    [menu.main.params]
        icon = "home"
        newTab = true
```

或者 YAML 示例：

```yaml
menu:
    main:
        - identifier: home
          name: Home
          url: /
          weight = -100
          params:
            icon: home
            newTab: true
```

* `identifier`: 项 ID
* `name`: 显示文本
* `url`: 链接
* `weight`: 项的优先级，值越低优先级越高。
* `params`: 
  * `icon`: 指定应使用的 SVG 图标
  * `newTab`: 在新标签页中打开此链接

如果 `params.icon` 设置为 `archive`，主题将会在 `assets/icons` 文件夹下查找 `archive.svg`。

## 添加自定义图标

此主题附带了一些来自 [Tabler Icons](https://tabler-icons.io) 的 SVG 图标。您可以在主题文件夹的 `assets/icons` 下找到它们。

要包含更多图标，只需从上述网站下载并将其放置在 Hugo 站点的 `assets/icons` 文件夹中即可。
