# express()

创建一个Express应用程序。`express()` 函数是express模块导出的最高层函数。

```javascript
var express = require('express');
var app = express();
```

## Methods

### express.json([options])

> 该中间件在Express v4.16.0之后可用

这是Express里面内置的中间件函数，它使用JSON解析传入请求，并且基于 [body-parser](http://expressjs.com/en/resources/middleware/body-parser.html)。

返回仅解析JSON并只查看内容类型标头与类型选项匹配的请求的中间件。该解析器接受主体的任何Unicode编码，并支持gzip和deflate编码的自动膨胀。