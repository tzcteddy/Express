# Hello world example

> 下面代码的就是你能创建的最简单的Express应用程序。它是一个单独的文件应用程序。如果您使用[Express generator](https://github.com/quxiaodong/express/blob/master/Getting%20started/%E7%94%9F%E6%88%90%E5%99%A8.md)，它将创建一个完整的应用程序脚手架，包括JavaScript文件、Jade模板和用于各种目的的子目录。

```javascript
const express = require('express')
const app = express()
const port = 3000

app.get('/', (req, res) => res.send('Hello World!'))

app.listen(port, () => console.log(`Example app listening on port ${port}!`))
```

这个应用程序启动一个服务器，并在端口3000上监听连接。当对根URL(/)或路由发起请求时，该应用程序回复“Hello World!”。对于其他路径，它将回复 **404 Not Found** 。

上面的示例实际上是一个正在运作的服务器：继续并单击显示的URL。您将得到一个响应回复，并且页面上有实时日志，并且您所做的任何更改都将实时反映出来。这是由 [RunKit](https://runkit.com/home) 提供的，它提供了一个交互式JavaScript运行环境，该运行环境连接到运行在Web浏览器中的完整Node环境。下面是在本地计算机上运行相同应用程序的说明。

> RunKit是不属于Express项目的第三方服务。

## 运行本地程序

一开始，我们创建了一个名为myapp的目录，进入目录，并运行 `npm init` 。然后根据[安装指南](https://github.com/quxiaodong/express/blob/master/Getting%20started/%E5%AE%89%E8%A3%85.md)将express安装为依赖项。

在myapp目录中，创建一个名为app.js的文件，并复制上面示例的代码。

> req（请求）和res（响应）是Node提供的完全相同的对象，因此在没有Expess的参与下，您可以调用req.pipe()、req.on('data', callback)做任何事情。

使用以下命令运行应用程序：

```
$ node app.js
```

然后，使用浏览器登录http://localhost:3000 来观察输出的内容。