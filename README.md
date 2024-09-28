# Hexo 博客模板

这是一个基于 [Hexo](https://hexo.io/) 及其主题 [Redefine](https://redefine-docs.ohevan.com/introduction) 的博客模板及部署教程, 成本为零, 无需服务器、域名、备案等. 最终成品参见 [我的博客](https://blog.leafyee.xyz/)

如果您没时间自己操作, 想要小叶子线下帮你操作或手把手教学, 欢迎联系我~ (价格好说)

## 使用说明

### 1 安装 [Node.js](https://nodejs.org/) 和 [Git](https://git-scm.com/)

`Node.js` 是一个 `JavaScript` 的运行环境 (类似于 `Python` 环境之于 `Python` 代码), 您将需要用它来本地运行 `Hexo`

`Git` 是一个分布式版本控制系统, 您将需要用它来上传您的博客到 `GitHub`

### 2 注册 [GitHub](https://github.com/) 和 [Cloudflare](https://www.cloudflare.com/)

`GitHub` 是一个免费的代码托管平台, 您将需要用它来存放您的博客源码和文章

`Cloudflare` 是一个免费的网络服务提供商 `赛博菩萨`, 您将会把您的博客部署到它的 `Pages` 服务器上

### 3 在 GitHub 上 Fork 本仓库

现在请登录您刚刚注册的 `GitHub` 账号, 点击本仓库右上角的 `Fork` 按钮, 将本仓库复制到您的账号下

### 4 将 Fork 后的仓库 Clone 到本地

首先创建一个文件夹用于存放您的博客, 然后请在这个文件夹下打开终端 (`Windows` 进入文件夹后鼠标右键选择 `在终端中打开` 类似的选项, `Mac` 在访达下方的文件夹路径处鼠标右键选择 `在终端中打开` 类似的选项), 并执行下面的命令

```bash
# 克隆你的博客到本地, 请将 xxx 替换为您的 GitHub 用户名 (区分大小写)
git clone https://github.com/xxx/HexoTemplate.git
```

> 如果您还是不清楚如何在制定文件夹打开终端, 请下载并安装 [VSCode](https://code.visualstudio.com/), 并在其中打开你想要存放博客的文件夹, 此时使用 `VSCode` 内置的终端即可 (那个终端的工作目录默认就是你打开的文件夹)

### 5 进入项目目录并安装依赖

一个程序往往会依赖于其他程序 (比如 `Python` 程序可能会依赖于 `numpy`、`pandas` 等库), 您需要安装这些依赖才能运行程序; `JavaScript` 程序也是如此

您需要进入**刚刚克隆下来的文件夹 `HexoTemplate`** 并执行下面的命令 (注意: 不是上一步的 `Blog` 文件夹, 而是 `Blog` 文件夹下的 `HexoTemplate` 文件夹). 后面的命令也是在这个文件夹下执行

```bash
# 安装依赖
npm install
```

> 同样, 如果您不清楚具体的文件路径, 请使用 `VSCode` 打开 `HexoTemplate` 文件夹

### 6 本地预览你的博客

要在本地预览你的博客, 请执行下面的命令; 执行后, 请不要关闭终端, 否则预览也会关闭; 如果要退出预览, 请在终端中按下 `Ctrl + C`

您现在可以在浏览器中输入 `localhost` 地址来预览您的博客, 在修改后, 刷新页面即可看到修改后的效果

```bash
npm run dev
```

### 7 新建文章

```bash
npx hexo new post 文章标题
```

> 文章语法见本模板中自带的那篇文章

### 8 新建页面

```bash
npx hexo new page 页面标题
```

> `页面` 与 `文章` 的区别在于, `页面` 不会出现在首页的文章列表中, 适合用来写一些静态的内容, 比如 `关于我` 页面; `页面` 的链接就是 `域名/页面标题`

### 8 将本地修改推送到 GitHub

在你的电脑上写的文章并不会自动同步到 `GitHub`, 您需要执行下面的命令将修改推送到 `GitHub`

```bash
npm run deploy
```

### 9 部署到 Cloudflare Pages

为了让您和他人的计算机都能够通过互联网访问您的博客, 您需要将您的博客部署到 `Cloudflare` 的 `Pages` 服务器上

首先, 请登录您的 `Cloudflare` 账号, 并在 `Cloudflare` 中创建一个新的 Pages 项目, 将 `GitHub` 仓库与之关联, 设置构建命令为 `npm run build`, 设置输出目录为 `public`

部署后你会得到一个 `Cloudflare` 提供的域名, 此时任何人都能通过 `xxx.pages.dev` 访问你的博客

> 如果您想要绑定自己的域名, 可以自行搜索域名购买教程 (也可直接在 `Cloudflare` 中购买, 但需要外币信用卡/外币储蓄卡)

### 10 进一步定制

你可以修改 `_config.redefine.yml` 和 `_config.yml` 文件来定制你的博客, 详见 [Redefine主题文档](https://redefine-docs.ohevan.com/introduction) 和 [Hexo文档](https://hexo.io/zh-cn/docs/)

您也可以进一步学习 `HTML`、`CSS`、`JavaScript` 等前端知识, 以实现更多的功能, 参见 [我的博客](https://blog.leafyee.xyz/)
