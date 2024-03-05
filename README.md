Refs CLI
===

<!--rehype:ignore:start-->
[![Buy me a coffee](https://img.shields.io/badge/Buy%20me%20a%20coffee-048754?logo=buymeacoffee)](https://jaywcjlove.github.io/#/sponsor)
[![CI](https://github.com/jaywcjlove/refs-cli/actions/workflows/ci.yml/badge.svg)](https://github.com/jaywcjlove/refs-cli/actions/workflows/ci.yml)
[![NPM version](https://img.shields.io/npm/v/refs-cli.svg?style=flat)](https://npmjs.org/package/refs-cli)
[![Repo Dependents](https://badgen.net/github/dependents-repo/jaywcjlove/refs-cli)](https://github.com/jaywcjlove/refs-cli/network/dependents)
[![Downloads](https://img.shields.io/npm/dm/refs-cli.svg?style=flat)](https://www.npmjs.com/package/refs-cli)
<!--rehype:ignore:end-->

Command line tool to generate `Quick Reference` website. This is also a tool separated from [`Quick Reference`](https://jaywcjlove.github.io/reference) to help [`Quick Reference`](https://jaywcjlove.github.io/reference) compile and generate HTML websites

<!--rehype:ignore:start-->
[![Quick Reference](https://user-images.githubusercontent.com/1680273/201931931-d8559417-0a15-46af-a009-ec1e56e5b778.png)](https://jaywcjlove.github.io/reference)
<!--rehype:ignore:end-->

## Document

[Reference English](./docs/quickreference.md)<!--rehype:style=background: rgb(92 107 192);&class=contributing&data-info=👆See what's missing?-->   
[Reference 中文](https://jaywcjlove.github.io/reference/docs/quickreference.html)<!--rehype:style=background: rgb(139 170 229);&class=contributing-->   
[Django](./docs/django.md)<!--rehype:style=background: rgb(12 75 51/var(\-\-bg\-opacity));&class=tag&class=contributing&data-lang=Python&data-info=See what's-->
<!--rehype:class=home-card-->

## Example Show

[Bash](https://jaywcjlove.github.io/reference/docs/bash.html)<!--rehype:style=background: rgb(72 143 223);-->  
[C](https://jaywcjlove.github.io/reference/docs/c.html)<!--rehype:style=background: rgb(92 107 192);-->  
[C#](https://jaywcjlove.github.io/reference/docs/cs.html)<!--rehype:style=background: rgb(6 147 13);&class=contributing-->  
[C++](https://jaywcjlove.github.io/reference/docs/cpp.html)<!--rehype:style=background: rgb(6 147 13);&class=contributing-->  
[Dart](https://jaywcjlove.github.io/reference/docs/dart.html)<!--rehype:style=background: rgb(64 196 255);-->  
[Docker](https://jaywcjlove.github.io/reference/docs/docker.html)<!--rehype:style=background: rgb(72 143 223);-->  
[Dockerfile](https://jaywcjlove.github.io/reference/docs/dockerfile.html)<!--rehype:style=background: rgb(0 72 153);&class=tag&data-lang=Docker-->  
[Django](https://jaywcjlove.github.io/reference/docs/djiango.html)<!--rehype:style=background: rgb(12 75 51);&class=contributing tag&data-lang=Python-->  
[Flutter](https://jaywcjlove.github.io/reference/docs/flutter.html)<!--rehype:style=background-image: linear-gradient(to left, rgba(236 72 153 / var(\-\-bg\-opacity)), rgba(167 139 250 / var(\-\-bg\-opacity)));&class=contributing tag&data-lang=Dart-->  
[Golang](https://jaywcjlove.github.io/reference/docs/golang.html)<!--rehype:style=background-image: linear-gradient(to left, rgba(74 222 128 / var(\-\-bg\-opacity)), rgba(59 130 246 / var(\-\-bg\-opacity)));-->  
<!--rehype:class=home-card-->

<!--rehype:ignore:start-->
## Command Help

```bash
Usage: refs-cli [output-dir] [--help|h]

  Displays help information.

Options:

  --version, -v   Show version number
  --help, -h      Displays help information.
  --watch, -w     Watch and compile Markdown files.
  --output, -o    Output directory. defalut(dist)
  --force, -f     Force file regeneration.

Example:

  $ npx refs-cli
  $ refs-cli --watch
  $ refs-cli --output website
  $ refs-cli

refs-cli@v0.0.1
```

## Config

Store `.refsrc.json` in the root directory of the project

```json
{
  "title": "Refs CLI",
  "description": "{{description}}. Sharing Quick Reference Cheat Sheets for Developers",
  "keywords": "reference-cli,reference,refs-cli,refs,cli",
  "data-info": "👆👆need your participation",
  "search": {
    "label": "Search",
    "placeholder": "Search for cheatsheet",
    "cancel": "Cancel"
  },
  "editor": {
    "label": "Edit"
  },
  "github": {
    "url": "https://github.com/jaywcjlove/refs-cli"
  },
  "home": {
    "label": "Home",
    "url": "https://jaywcjlove.github.io/refs-cli"
  },
  "giscus": {
    "src": "https://giscus.app/client.js",
    "data-repo": "jaywcjlove/refs-cli",
    "data-repo-id": "R_kgDOIfibtA",
    "data-category": "Q&A",
    "data-category-id": "DIC_kwDOIfibtM4CZObA",
    "data-mapping": "pathname",
    "data-strict": "0",
    "data-reactions-enabled": "1",
    "data-emit-metadata": "0",
    "data-input-position": "bottom",
    "data-theme": "preferred_color_scheme",
    "data-lang": "en",
    "crossorigin": "anonymous",
    "async": true
  }
}
```

Support adding [`giscus`](https://giscus.app) comments.

Support [JSON](https://www.json.org), [JSONC](https://github.com/microsoft/node-jsonc-parser), [JSON5](https://json5.org/), [YAML](https://yaml.org/), [TOML](https://toml.io), [INI](https://en.wikipedia.org/wiki/INI_file), [CJS](http://www.commonjs.org), [Typescript](https://www.typescriptlang.org/), and ESM config load.

`TOML` config example:

```toml
title = "Refs CLI"
description = "{{description}}. Sharing Quick Reference Cheat Sheets for Developers"
keywords = "reference-cli,reference,refs-cli,refs,cli"
data-info = "👆👆need your participation"
[search]
  label = "Search"
  placeholder = "Search for cheatsheet"
  cancel = "Cancel"

[editor]
  label = "Edit"
[github]
  url = "https://github.com/jaywcjlove/refs-cli"
[home]
  label = "Home"
  url = "https://jaywcjlove.github.io/refs-cli"
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

## Thanks to all contributors1
<!--rehype:wrap-style=text-align: center;max-width: 650px;margin: 0 auto;&class=home-title-reset-->

See [Quick Reference](./docs/quickreference.md) for how to get started. As always, thanks to our amazing contributors!
<!--rehype:style=padding-bottom:1rem;-->

<!--GAMFC--><a href="https://github.com/jaywcjlove" title="小弟调调">
  <img src="https://avatars.githubusercontent.com/u/1680273?v=4" width="42;" alt="小弟调调"/>
</a>
<a href="https://github.com/renxia" title="任侠">
  <img src="https://avatars.githubusercontent.com/u/2276421?v=4" width="42;" alt="任侠"/>
</a><!--GAMFC-END-->

List of contributors, automatically generated by [contributors](https://github.com/jaywcjlove/github-action-contributors)
<!--rehype:style=padding-top:1rem;-->

## Mirror site of Quick Reference1
<!--rehype:wrap-style=text-align: center;max-width: 650px;margin: 0 auto;&class=home-title-reset-->

[quickref.cn](https://quickref.cn)<!--rehype:target=_blank-->
[ecdata.cn](http://ref.ecdata.cn)<!--rehype:target=_blank-->
[aibk.cn](https://quickref.aibk.cn)<!--rehype:target=_blank-->
[jgeek.cn](http://reference.jgeek.cn/)<!--rehype:target=_blank-->
[laoleng.vip](http://bbs.laoleng.vip/reference/)<!--rehype:target=_blank-->
[liujiapeng.com](https://www.liujiapeng.com/)<!--rehype:target=_blank-->

<!--rehype:class=home-card home-links-->


<!--rehype:ignore:start-->
## License

MIT © [Kenny Wong](https://github.com/jaywcjlove)
<!--rehype:ignore:end-->
