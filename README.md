# Hexo 博客模板

## 使用说明

### 1 安装 [Node.js](https://nodejs.org/) 和 [Git](https://git-scm.com/)

### 2 注册 [GitHub](https://github.com/) 和 [Cloudflare](https://www.cloudflare.com/)

### 3 在 GitHub 上 Fork 本仓库

### 4 将 Fork 后的仓库 Clone 到本地

```bash
git clone https://github.com/xxx/HexoTemplate.git # xxx 为你的 GitHub 用户名
```

> 注意, 请在你想要存放博客的目录下执行上面的命令

### 5 进入项目目录并安装依赖

```bash
cd ./HexoTemplate
npm install
```

### 6 本地预览你的博客

```bash
npm run dev
# 如果要退出预览, 请在终端中按下 Ctrl + C
```

> 运行上面的命令后, 在浏览器中打开 `localhost` 地址即可预览

### 7 新建文章

```bash
npx hexo new post 文章标题
```

> 文章语法见本模板中自带的那篇文章

### 8 将本地修改推送到 GitHub

```bash
npm run deploy
```

> 每次修改后, 都需要运行上面的命令将修改推送到 GitHub, 你的博客才会更新

### 9 部署到 Cloudflare Pages

在 `Cloudflare` 中创建一个新的 Pages 项目, 并将 `GitHub` 仓库与之关联, 设置构建命令为 `npm run build`, 设置输出目录为 `public`

> 部署后你会得到一个 `Cloudflare` 提供的域名, 任何人都能通过 `xxx.pages.dev` 访问你的博客

### 10 进一步定制

你可以修改 `_config.redefine.yml` 和 `_config.yml` 文件来定制你的博客, 详见 [Redefine主题文档](https://redefine-docs.ohevan.com/introduction) 和 [Hexo文档](https://hexo.io/zh-cn/docs/)
