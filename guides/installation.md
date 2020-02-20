# 安装

下面介绍安装 webpack 的各种办法。

## 前提条件

请先确保安装了 [Node.js](https://nodejs.org/en/) 的最新版本。建议使用 Node.js 最新的长期支持版本（LTS - Long Term Support）。使用旧版本可能遇到各种问题，因为它们可能缺少 webpack 功能/或缺少其他相关 webpack 包。

## 本地安装

要安装最新版本或特定版本，你需要运行以下命令：

``` bash
npm install --save-dev webpack # 安装最新版本
npm install --save-dev webpack@<version> # 安装特定版本
```

如果你使用的是 webpack 4+ 版本，你还需要安装 CLI：

``` bash
npm install --save-dev webpack-cli
```

本地安装的好处：

**在 webpack 引入破坏式变更(breaking change)时，更容易分别升级项目。**

通常，webpack 通过运行一个或多个 [npm scripts](https://docs.npmjs.com/misc/scripts)，会在本地 `node_modules` 目录中查找安装的 webpack：

``` json
"scripts": {
    "start": "webpack --config webpack.config.js"
}
```

> 当我们在本地安装 webpack 后，我们能够从 `node_modules/.bin/webpack` 访问它的 `bin` 版本。

## 全局安装

要在全局下安装 webpack，请运行下面命令：

``` bash
npm install --global webpack
```

> 不推荐全局安装 webpack，这会使你项目中的 webpack 锁定到指定版本，在使用 webpack 的不同项目中，可能导致构建失败。

## 体验最新版本

下面最新版本的 webpack 可能仍然包含 bug，不能用于生产环境。

``` bash
npm install webpack@beta
npm install webpack/webpack#<tabname/branchname>
```

----

> 参考：
>
> https://www.webpackjs.com/guides/installation/
>
> https://webpack.js.org/guides/installation/

----
