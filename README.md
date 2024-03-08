md-card-cli
===

<!--rehype:ignore:start-->
[![NPM version](https://img.shields.io/npm/v/md-card-cli.svg?style=flat)](https://npmjs.org/package/md-card-cli)
[![Downloads](https://img.shields.io/npm/dm/md-card-cli.svg?style=flat)](https://www.npmjs.com/package/md-card-cli)
<!--rehype:ignore:end-->

一个将`markdown`转换为卡片式`html`页面的命令行工具。

<!--rehype:ignore:start-->
[![Quick Start](https://github.com/ytanck/md-card-cli/assets/69585768/4767ef11-4723-42a1-b4aa-0452265ce830)](./docs/quickstart-zh.md)
<!--rehype:ignore:end-->

## Document

[中文文档](./docs/quickstart-zh.md)<!--rehype:style=background: rgb(92 107 192);&data-subtitle=我是中文文档&class=info subtitle&data-info=👆值得推荐的-->   
[英文文档](./docs/quickstart.md)<!--rehype:style=background: rgb(92 107 192);&data-subtitle=我是英文文档&class=subtitle-->     
[test](./docs/test.md)<!--rehype:style=background: rgb(92 107 192);-->  

<!--rehype:class=home-card-->

## Example Show

[科目一](https://ytanck.github.io/reference/docs/test.html)<!--rehype:style=background: rgb(72 143 223);&data-subtitle=我是副标题&class=info&data-info=👆click me !-->  
[科目二](https://ytanck.github.io/reference/docs/test.html)<!--rehype:style=background: rgb(92 107 192);&class=info subtitle&data-subtitle=我是副标题-->  
[科目三](https://ytanck.github.io/reference/docs/test.html)<!--rehype:style=background: rgb(6 147 13);&class=tag&data-tag=108课时-->  
[科目四](https://ytanck.github.io/reference/docs/test.html)<!--rehype:style=background: rgb(6 147 13);&class=tag&data-tag=经济-->  
[科目五](https://ytanck.github.io/reference/docs/test.html)<!--rehype:style=background: rgb(64 196 255);&class=subtitle&data-subtitle=详细信息请查看...-->  
[科目六](https://ytanck.github.io/reference/docs/test.html)<!--rehype:style=background: rgb(72 143 223);-->  
[科目七](https://ytanck.github.io/reference/docs/test.html)<!--rehype:style=background: rgb(0 72 153);&class=tag&data-tag=标签1-->  
[科目八](https://ytanck.github.io/reference/docs/test.html)<!--rehype:style=background: rgb(12 75 51);&class=info tag&data-tag=热门-->  
[科目九](https://ytanck.github.io/reference/docs/test.html)<!--rehype:style=background-image: linear-gradient(to left, rgba(236 72 153 / var(\-\-bg\-opacity)), rgba(167 139 250 / var(\-\-bg\-opacity)));-->  
[我是科目十](https://ytanck.github.io/reference/docs/test.html)<!--rehype:style=background-image: linear-gradient(to left, rgba(74 222 128 / var(\-\-bg\-opacity)), rgba(59 130 246 / var(\-\-bg\-opacity)));&class=subtitle&data-subtitle=我是渐变背景色-->  
<!--rehype:class=home-card-->

<!--rehype:ignore:start-->
## Command Help

```bash
Usage: md-card-cli [output-dir] [--help|h]

  Displays help information.

Options:

  --version, -v   Show version number
  --help, -h      Displays help information.
  --watch, -w     Watch and compile Markdown files.
  --output, -o    Output directory. defalut(dist)
  --force, -f     Force file regeneration.

Example:

  $ npx md-card-cli
  $ md-card-cli --watch
  $ md-card-cli --output website
  $ md-card-cli

md-card-cli@v0.0.1
```

## Config

Store `.refsrc.json` in the root directory of the project

```json
{
  "title": "md-card-cli",
  "description": "{{description}}. A command line tool to convert markdown to a card-html page !",
  "keywords": "reference-cli,reference,md-card-cli,html-cli,cli",
  "data-info": "👆click me !",
  "search": {
    "label": "Search",
    "placeholder": "Search for card",
    "cancel": "Cancel"
  },
  "network": {
    "label": "Blog",
    "url": "site",
    "disabled": false
  },
  "github": {
    "url": "https://github.com/ytanck/md-card-cli"
  },
  "home": {
    "label": "Home",
    "url": "https://ytanck.github.io/md-card-cli"
  },
  "giscus": {
    "src": "https://giscus.app/client.js",
    "data-repo": "ytanck/md-card-cli",
    "data-repo-id": "R_kgDOLb0Dow",
    "data-category": "Q&A",
    "data-category-id": "DIC_kwDOLb0Do84CdwWy",
    "data-mapping": "pathname",
    "data-strict": "0",
    "data-reactions-enabled": "1",
    "data-emit-metadata": "0",
    "data-input-position": "bottom",
    "data-theme": "preferred_color_scheme",
    "data-lang": "zh-CN",
    "crossorigin": "anonymous",
    "async": true
  }
}
```

Support adding [`giscus`](https://giscus.app) comments.

Support [JSON](https://www.json.org), [JSONC](https://github.com/microsoft/node-jsonc-parser), [JSON5](https://json5.org/), [YAML](https://yaml.org/), [TOML](https://toml.io), [INI](https://en.wikipedia.org/wiki/INI_file), [CJS](http://www.commonjs.org), [Typescript](https://www.typescriptlang.org/), and ESM config load.

`TOML` config example:

```toml
title = "md-card-cli"
description = "{{description}}. A command line tool to convert markdown to a card-html page !"
keywords = "reference-cli,reference,md-card-cli,refs,cli"
data-info = "👆click me"
[search]
  label = "Search"
  placeholder = "Search for content"
  cancel = "Cancel"

[network]
  label = "Blog"
  url = "site"
  disabled = false
[github]
  url = "https://github.com/ytanck/md-card-cli"
[home]
  label = "Home"
  url = "https://ytanck.github.io/md-card-cli"
```

Support for more config loading.

```bash
.refsrc                    .refsrc.json
.refsrc.json5              .refsrc.jsonc
.refsrc.yaml               .refsrc.yml
.refsrc.toml               .refsrc.ini
.refsrc.js                 .refsrc.ts
.refsrc.cjs                .refsrc.mjs
.config/refsrc             .config/refsrc.json
.config/refsrc.json5       .config/refsrc.jsonc
.config/refsrc.yaml        .config/refsrc.yml
.config/refsrc.toml        .config/refsrc.ini
.config/refsrc.js          .config/refsrc.ts
.config/refsrc.cjs         .config/refsrc.mjs
refs.config.js             refs.config.ts
refs.config.cjs            refs.config.mjs
```
<!--rehype:ignore:end-->


## 友情链接
<!--rehype:wrap-style=text-align: center;max-width: 650px;margin: 0 auto;&class=home-title-reset-->

[baidu.com](https://baidu.com)<!--rehype:target=_blank-->
[github](https://github.com)<!--rehype:target=_blank-->
[youtube](http://youtube.com)<!--rehype:target=_blank-->
[gitee](http://gitee.com)<!--rehype:target=_blank-->

<!--rehype:class=home-card home-links-->


<!--rehype:ignore:start-->
## License

MIT © [ytanck](https://github.com/ytanck)
<!--rehype:ignore:end-->
