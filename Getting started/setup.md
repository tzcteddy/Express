# 安装

假设你已经安装了[Node.js](https://nodejs.org/en/)，创建一个目录来保存你的应用程序，并将其作为工作目录。

```
$ mkdir myapp
$ cd myapp
```

使用 `npm init` 命令为应用程序创建一个package.json文件。有关package.json如何运作的详细信息，请参阅npm的[package.json处理的详细信息](https://docs.npmjs.com/files/package.json)。

```
$ npm init
```

此命令提示您执行许多操作，例如应用程序的名称和版本。现在，您可以简单地单击 `RETURN` 来接受大多数默认值，但有以下例外：

```
entry point: (index.js)
```

输入app.js，或者您希望主文件的名称是什么。如果希望它是index.js，请单击 `RETURN` 接受建议的默认文件名。

现在进入myapp目录中安装Express并将其保存在依赖项列表中。例如：

```
$ npm install express --save
```

要临时安装Express，而不将其添加到依赖项列表：

```
$ npm installl express --no-save
```

> npm 5.0+ 版本在默认情况下会将安装的模块添加到 package.json 文件中的 dependencies 列表中。对于较老的 npm 版本，你就必须指定 --save 参数。然后，照旧执行 npm install 命令即可自动安装依赖列表中所列出的所有模块。