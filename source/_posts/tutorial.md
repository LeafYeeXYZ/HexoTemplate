---
title: 博客文章书写教程
excerpt: 这是本模板的自带文章，用于展示如何书写博客文章
date: 2024-01-01 10:00:00
categories: 文章分类
tags: [文章标签1,文章标签2,文章标签3]
---

本文在[这篇文章](https://blog.leafyee.xyz/2023/10/26/MarkdownHTML文章写作/)的基础上有所增减, 亦欢迎阅读原文章学习更多内容

# 基础

`Markdown` 是一种轻量级标记语言, 它允许人们使用易读易写的纯文本格式编写文档, 然后通过渲染器自动转换成 `HTML` 文档

由于 `Markdown` 的轻量化、易读易写特性, 并且对于图片、图表、数学式都有支持, 许多网站都广泛使用 `Markdown` 来撰写帮助文档或是用于论坛上发表消息, 如 `GitHub`、`简书`、`CSDN`

`Hexo` 是一个基于 `Node.js` 的静态博客框架, 通过 `Markdown` 文件生成静态网页, 并且支持 `Git` 部署, 使得博客的搭建和维护变得更加简单

下面的内容将介绍 `Markdown` 的基本语法, 以及 `Hexo` 的主题 `Redefine` 的一些高级功能

## 标题

```markdown
# 一级标题

## 二级标题

以此类推, 最大到六级标题
```

## 段落

```markdown
我是第一个段落
我也是第一个段落（空格）
我和上一行之间只会显示一个空格（空格）（空格）
我和上一行之间会显示一个空行

我是第二个段落
我和第一个段落之间会显示比一个空行更高的间距

# 标题

我是第三个段落
书写图片、列表、表格、分割线等内容时
应使它们前后各空一行

![我是一张图片](xxxxx)

我是第四个段落
```

> 简而言之, 请把你的文章各部分内容想象成一个个的**块**, **块**可以是**段落**、**标题**、**列表**、**表格**等等, **块**之间用空行隔开

## 字形

| 效果 | Markdown |
| :---: | :---: |
| *斜体* | \*斜体\* |
| **粗体** | \*\*粗体\*\* |
| ***粗斜体*** | \*\*\*粗斜体\*\*\* |
| <u>下划线</u> | \<u\>下划线\</u\> |
| ~~删除线~~ | \~\~删除线\~\~ |
| <mark>高亮</mark> | \<mark\>高亮\</mark\> |
| 上脚注<sup>上脚注</sup> | 上脚注\<sup\>上脚注\</sup\> |
| 下脚注<sub>下脚注</sub> | 下脚注\<sub\>下脚注\</sub\> |

## 列表

```markdown
- 无序列表
  - 每级多一个缩进
    - 用 * + - 都可以表示

- [ ] 任务列表
- [x] 加x是已完成
- [ ] 加空格是未完成

> 引用内容
>> 每级多一个箭头
>>> 这是第三级

1. 有序列表
  1. 可以有多级
  2. 同级缩进相同
2. 每级多一个缩进
```

- 无序列表
  - 每级多一个缩进
    - 用 * + - 都可以表示

---

- [ ] 任务列表
- [x] 加x是已完成
- [ ] 加空格是未完成

---

> 引用内容
>> 每级多一个箭头
>>> 这是第三级

---

1. 有序列表
  1. 可以有多级
  2. 同级缩进相同
2. 每级多一个缩进

## 链接

普通的链接形如: `[Github](https://github.com)`, 效果是: [Github](https://github.com) (显示链接文字)

也可以这样写: `<https://github.com>`, 效果是: <https://github.com> (直接显示链接)

## 图片

你的博客文件中的 `source` 文件夹应当是你所有图片、文章、资源的存放地; 为了清晰, 可以在 `source` 文件夹下再建立一个 `images` 文件夹, 专门用来存放图片

例如, 你的图片路径是 `source/001.png`, 那么在文章中引用图片的写法是 `![](/001.png)`; 如果图片路径是 `source/images/001.png` (即 `source` 文件夹下的 `images` 文件夹下的 `001.png`), 那么在文章中引用图片的写法是 `![](/images/001.png)`

## 代码

`像这样的单行代码` 的写法是: \`像这样的单行代码\`

~~~markdown
```代码类型
多行代码
代码类型不写则默认为普通文本
单行和多行代码代码内部的特殊符号不会被解析
并且会原封不动地展示换行、缩进、空格等格式
```

例如:

```python
def hello():
  print("Hello, World!")
```
~~~

```python
def hello():
  print("Hello, World!")
```

## 表格

```markdown
| 标题-左对齐 | 标题-中对齐 | 标题-右对齐 |
| :- | :-: | -: |
| 如果自己写 | 嫌麻烦的话 | 可以用生成工具 |
| 记得代码的 | 第二行 | 是`-` |
```

| 标题-左对齐 | 标题-中对齐 | 标题-右对齐 |
| :- | :-: | -: |
| 如果自己写 | 嫌麻烦的话 | 可以用[生成工具](https://www.tablesgenerator.com/markdown_tables) |
| 记得代码的 | 第二行 | 是`-` |

## 其他

- 分割线为 `---`, 前后空一行再输入分割线; 也可用 `<hr>` 表示
- 用转义字符 `\` 来避免解析 `# * - > [ (` 等特殊符号 (即如果想要显示 `#` 则写成 `\#`)
- `VScode` 中, 按 `Ctrl`+`Shift`+`V` 可实时预览 `.md` 文件

# 进阶

{% note yellow %}
**本部分内容仅适用于 `Hexo` 博客框架的 `Redefine` 主题**
{% endnote %}

## 文章自定义

- **文章加密**: 利用`encrypt`插件可以对文章进行加密, 只需在`Front-matter`中添加`password: xxxxx`即可
- **文章置顶**: 在`Front-matter`中添加`sticky: xxx`, `xxx`的数值越大, 置顶的文章越靠前
- **首页略缩图**: 在`Front-matter`中添加`thumbnail: "/images/xxx.jpg"`
- **文章封面**: <br>在`Front-matter`中添加`cover/banner: "/iamges/xxx.jpg"`, `cover/banner`二者选其一即可<br>如果`thumbnail`和`cover/banner`只存在一个, 则另一个也会被自动设置为存在的那个设置的图片<br>要只保留一个, 则可把另一个设置为`: false`
- **文章时效性**: 在`Front-matter`中添加`expires: YYYY-MM-DD HH:MM:SS`, 在超过此日期后, 用户会看到文章时效性提示

## 选项卡

```markdown
{% tabs 页面内唯一名称 %}
<!-- tab 栏目1 -->
内容1
<!-- endtab -->
<!-- tab 栏目2 -->
内容2
<!-- endtab -->
<!-- tab 栏目3 -->
内容3
<!-- endtab -->
{% endtabs %}
唯一名称建议用中文
```

{% tabs 唯一名称 %}
<!-- tab 栏目1 -->
*内容1*
<!-- endtab -->
<!-- tab 栏目2 -->
**内容2**
<!-- endtab -->
<!-- tab 栏目3 -->
***内容3***
<!-- endtab -->
{% endtabs %}

## 提示块

```markdown
{% notel red fa-info 标题 %}
这是大号提示块
图标选填
注意图标只填后半部分
{% endnotel %}
```

{% notel red fa-info 标题 %}
这是大号提示块, 图标选填
注意图标只填后半部分
{% endnotel %}

```markdown
{% note red fa-info %}
这是小号提示块, 同样图标选填
{% endnote %}
```

{% note red fa-info %}
这是小号提示块, 同样图标选填
{% endnote %}

## 按钮

```markdown
{% btn 大小::名称::URL::图标 %}
大小和图标选填, 不同大小见下方
```

{% btn 无参数::#按钮 %}
{% btn regular::regular::#按钮 %}
{% btn large::large::#按钮 %}
{% btn center::center::#按钮 %}
{% btn center large::center large::#按钮 %}
{% btn center regular::center regular::#按钮 %}

## 折叠

```markdown
{% folding red::标题 %}
折叠内容
{% endfolding %}
```

{% folding red::标题 %}
折叠内容
{% endfolding %}
