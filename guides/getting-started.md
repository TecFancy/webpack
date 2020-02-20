# 起步

webpack 用于编译 JavaScript 模块。一旦完成[安装](/guides/installation.md)，你就可以通过 webpack 的 [CLI](/api/cli.md) 或 [API](/api/node.md) 与其配合交互。如果你还不熟悉 webpack，请阅读[核心概念](/concepts/README.md)和[打包器对比](/comparison/README.md)，了解为什么你要使用 webpack，而不是社区中的其他工具。

## 基本安装

首先，我们创建一个目录，初始化 npm，然后 [在本地安装](/guides/installation.html#本地安装)，接着安装 webpack-cli(此工具用于在命令行中运行 webpack)：

``` bash
mkdir webpack-playground && cd webpack-playground
npm init -y
npm install --save-dev webpack webpack-cli
```

现在，我们创建以下目录结构、文件和内容：

**project**
``` none
webpack-playground
|- package.json
|- index.html
|- /src
  |- index.js
```

**src/index.js**
``` javascript 
function component() {
  var element = document.createElement('div');

  // Lodash（目前通过一个 script 脚本引入）对于执行这一行是必须的
  element.innerHTML = _.join(['Hello', 'webpack'], ' ');

  return element;
}

document.body.appendChild(component);
```

**index.html**
``` html 
<!doctype html>
<html>
  <head>
    <title>起步</title>
    <script src="https://unpkg.com/lodash@4.16.6"></script>
  </head>
  <body>
    <script src="./src/index.js"></script>
  </body>
</html>
```
