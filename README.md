# Hexo-theme-diaspora / @WhiteRobe modified

- 2019-9-5:修改/Fork自[Fechin/hexo-theme-diaspora](https://github.com/Fechin/hexo-theme-diaspora)，在此基础上做了我的修改。
- 适配Katex，需要在hexo目录下执行：

``` bash
cd ..
npm un hexo-renderer-marked --save
npm i hexo-renderer-markdown-it-plus --save
```

---

一款基于WP移植的Hexo主题，主题干净而又清新，适合喜欢摄影、影评、乐评和玩弄文字的你。 [在线预览 | PREVIEW ](http://fech.in)

> 再次感谢原作者创作出这么精美的主题 [@Loeify](https://github.com/LoeiFy/Diaspora) 。如果你喜欢，请捐助原作者。

![cover](https://fech.in/static/images/Diaspora.jpg)

## 快速上手 Quick-Start

### 主题相关 Usage

**安装主题 Installation**

``` bash
cd /themes
$ git clone git@github.com:WhiteRobe/hexo-theme-diaspora.git wr-diaspora
```


**启用主题 Enable Theme**

修改Hexo配置文件 `_config.yml` 主题项设置为`wr-diaspora`

``` yaml
...
theme: wr-diaspora
...
```

**更新主题 Update Theme**

> 注意：请在更时主题时备份`_config.yml`配置文件

``` bash
cd themes/wr-diaspora
git pull
```

### 初始化 Initialization

**Step.1 新建文章模板**

``` markdown
---
title: {{ title }}
date: {{ date }}
categories: 
    - 分类1
    - 分类2
tags: 
    - 标签1
    - 标签2
mp3: http://example.com/example.mp3
cover: http://example.com/example.jpg
description: 'description(不超过60字)'
---
```

**Step.2 创建分类页**
1. 新建一个页面，命名为`categories`。命令如下：
```
hexo new page categories
```
2. 编辑刚新建的页面，将页面的类型设置为`categories`：
```
---
title: categories
date: 2014-12-22 12:39:04
type: "categories"
---
```
主题将自动为这个页面显示所有分类。

**Step.3 创建标签页**

1. 新建一个页面，命名为`tags` 。命令如下：
```
hexo new page tags
```
2. 编辑刚新建的页面，将页面的类型设置为`tags`：
```
---
title: tags
date: 2014-12-22 12:39:04
type: "tags"
---
```
主题将自动为这个页面显示所有标签。

### 启用站内搜索注意事项

需要配置相关的Aloglia账号，并更新你的索引，索引格式的样例为：

```json
{
    "title": "好用又好看的终端——Terminus",
    "url": "/2019/10/05/zh/terminus-intro/",
    "keys":" 软件推荐"
}
```




## 主题配置 Theme Configure
```yml
# 头部菜单，title: link
menu:
  Github: {{Your github}}
  分类: /categories
  归档: /archives
  标签云: /tags

# 是否显示目录
TOC: false

# 是否自动播放音乐
autoplay: false

# 站内检索API，使用了algolia的服务
algoliaApp: '$APPKEY'
algoliaKey: '$SEARCHKEY'
algoliaIndice: '$INDICE'

# 默认音乐（随机播放）
mp3: 
  - http://link.hhtjim.com/163/425570952.mp3
  - http://link.hhtjim.com/163/425570952.mp3

# 首页封面图, 为空时取文章的cover作为封面
welcome_cover: # /img/welcome-cover.jpg

# 默认文章封面图
cover: /img/cover.jpg

# Gitalk 评论插件（https://github.com/gitalk/gitalk）
gitalk:
    # 是否自动展开评论框
    autoExpand: false
    # 应用编号
    clientID: ''
    # 应用秘钥
    clientSecret: ''
    # issue仓库名
    repo: ''
    # Github名
    owner: ''
    # Github名
    admin: ['']
    # Ensure uniqueness and length less than 50
    id: location.pathname
    # Facebook-like distraction free mode
    distractionFreeMode: false

# 网站关键字
keywords: Fechin, WhiteRobe

# 要使用google_analytics进行统计的话，这里需要配置ID
google_analytics: 

# 网站ico
favicon: /img/favicon.png

# rss文件
rss: atom.xml
```

