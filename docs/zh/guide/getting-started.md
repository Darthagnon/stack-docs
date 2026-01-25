# 开始使用

::: tip
试试这个快速入门模板，在几分钟内即可开始使用 Stack 和 Hugo：
https://github.com/CaiJimmy/hugo-theme-stack-starter
:::

## 环境要求
在开始之前，请确保您已经安装了 Hugo **extended 版本**。更多信息请参阅 [Hugo 官方文档](https://gohugo.io/getting-started/installing/)。

此主题使用了 SCSS 和 TypeScript，因此需要 Hugo extended 版本。如果您使用的是非 extended 版本，将会遇到以下错误：

```
Error: Error building site: TOCSS: failed to transform "scss/style.scss" (text/x-scss): this feature is not available in your current Hugo version
```

安装 Hugo 后，您可以通过运行以下命令来检查版本：

```bash
hugo version
```

输出应类似于以下内容（版本号可能不同），请注意 `extended` 关键字：

```
hugo v0.102.3-b76146b129d7caa52417f8e914fc5b9271bf56fc+extended windows/amd64 BuildDate=2022-09-01T10:16:19Z VendorInfo=gohugoio
```

最低要求的 Hugo 版本可以在 [主题的 `theme.toml` 文件](https://github.com/CaiJimmy/hugo-theme-stack/blob/master/theme.toml#L23) 中查看。

## 安装

### Git
在 master 分支上，您可以找到主题的最新源代码。要使用最新版本，您可以运行以下命令将存储库克隆到 Hugo 站点的根目录下的 `themes/hugo-theme-stack`：

```bash
git clone https://github.com/CaiJimmy/hugo-theme-stack/ themes/hugo-theme-stack
```

如果您已经为站点使用了 Git，可以运行以下命令将主题添加为子模块：

```bash
git submodule add https://github.com/CaiJimmy/hugo-theme-stack/ themes/hugo-theme-stack
```

### Hugo 模块 (Hugo module)

::: warning
使用此方法，`themes` 目录下不会有任何文件。为了修改主题，您需要将想要修改的文件复制到 `layouts` 目录下对应的目录中。

例如，要修改 `themes/hugo-theme-stack/layouts/partials/header.html` 文件，您需要将其复制到 `layouts/partials/header.html` 并在那里进行修改（从主题仓库中复制原始代码）。这同样适用于 `assets` 和 `static` 目录。
:::

此主题也可以作为 [Hugo 模块](https://gohugo.io/hugo-modules/) 使用。在您的 Hugo 站点根目录下运行以下命令：

首先将您的站点初始化为 Hugo 模块（如果您还没有这样做）：

```sh
hugo mod init github.com/me/my-new-blog
```

然后通过在站点的配置文件中的 `module` 部分添加以下行来导入主题作为依赖项。

```toml
# config.toml
[[module.imports]]
path = "github.com/CaiJimmy/hugo-theme-stack/v3"
```

```yaml
# config.yaml
module:
  imports:
    - path: github.com/CaiJimmy/hugo-theme-stack/v3
```

这会使 Hugo 使用主题最新的稳定 `v3` 版本（在 release 页面提供，可能与 `master` 分支中的最新提交不一致）。

要将主题更新到最新版本，请运行以下命令：

```sh
hugo mod get -u github.com/CaiJimmy/hugo-theme-stack/v3
hugo mod tidy
```

::: info
将来，如果主题发布了新的大版本，您需要手动更新 `path` 字段中的版本号。
:::

### 手动下载 (不推荐)

您也可以从 [release 页面](https://github.com/CaiJimmy/hugo-theme-stack/releases) 下载主题并将其解压到 `themes/hugo-theme-stack` 目录中。