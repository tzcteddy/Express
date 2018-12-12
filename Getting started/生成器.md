# Express 应用程序生成器

通过应用生成器工具 express-generator 可以快速创建一个应用的骨架。

express-generator 包含了 express 命令行工具。通过如下命令即可安装：

```
$ npm install express-generator -g
```

可以通过 `-h` 参数列出所有可用的命令行参数：

```
$ express -h

  Usage: express [options] [dir]

  Options:

        --version        output the version number
    -e, --ejs            add ejs engine support
        --pug            add pug engine support
        --hbs            add handlebars engine support
    -H, --hogan          add hogan.js engine support
    -v, --view <engine>  add view <engine> support (dust|ejs|hbs|hjs|jade|pug|twig|vash) (defaults to jade)
        --no-view        use static html instead of view engine
    -c, --css <engine>   add stylesheet <engine> support (less|stylus|compass|sass) (defaults to plain css)
        --git            add .gitignore
    -f, --force          force on non-empty directory
    -h, --help           output usage information
```

例如，以下创建一个名为myapp的快速应用程序。该命令将在当前工作目录中创建一个名为myapp的文件夹，视图引擎（view engine）将设置为Pug：

```
$ express --view=pug myapp

  create : myapp\
  create : myapp\public\
  create : myapp\public\javascripts\
  create : myapp\public\images\
  create : myapp\public\stylesheets\
  create : myapp\public\stylesheets\style.css
  create : myapp\routes\
  create : myapp\routes\index.js
  create : myapp\routes\users.js
  create : myapp\views\
  create : myapp\views\error.pug
  create : myapp\views\index.pug
  create : myapp\views\layout.pug
  create : myapp\app.js
  create : myapp\package.json
  create : myapp\bin\
  create : myapp\bin\www

  change directory:
    > cd myapp

  install dependencies:
    > npm install

  run the app:
    > SET DEBUG=myapp:* & npm start
```

进入myapp，安装相应依赖：

```
$ cd myapp
$ npm install
```

在MacOS或Linux中，用以下命令运行程序：

```
$ DEBUG=myapp:* npm start
```

在Windows中，用以下命令：

```
> set DEBUG=myapp:* & npm start
```

依赖安装完成后，在浏览器中输入http://localhost:3000 来访问程序。

以下是通过生成器创建应用后的目录：

```
.
├── app.js
├── bin
│   └── www
├── node_modules
│   └── ...
├── package.json
├── public
│   ├── images
│   ├── javascripts
│   └── stylesheets
│       └── style.css
├── routes
│   ├── index.js
│   └── users.js
└── views
    ├── error.pug
    ├── index.pug
    └── layout.pug
```

> 通过 Express 应用生成器创建应用只是众多方法中的一种。你可以使用这个结构或对其进行修改以达到适合你的需要。