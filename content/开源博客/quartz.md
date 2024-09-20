[Github](https://github.com/jackyzha0/quartz)

## 参考教程

- [官方文档](https://quartz.jzhao.xyz/)

## 前置需求：

- 下载并安装 Git
- 注册 Github 帐号
- 注册 Cloudflare 帐号（可以不要）
- 域名 （也可以没有）

## 部署记录

1. 克隆仓库
	fork [jackyzha0/quartz](https://github.com/jackyzha0/quartz)
2. 删除文件
	下载项目，删除无用的文件/文件夹，如/doc。
3. 编写文档
	- 所有的内容放置在`/content`目录下，用 Markdown 语言书写。可以使用obsidian打开该目录。
	- 必须含有index.md。
1. 基础配置
	1. 在`quartz.config.ts`中配置整个网站的 pageTitle 和 baseUrl。如我这里的设置：  
	    `pageTitle: " Being Nobody",`  
	    `baseUrl: "garden.muxiao.org",`
    
	2. 在`quartz.layout.ts`中配置整个网站页面底部的展示链接。  
	    在 sharedPageComponents 条目下的 footer 下的 links 中设置。
5. 个性化设置
	1. 在`盘符:\你的项目名\quartz\static\`中放置网站的 ico 图标，和网站页面 logo 图片。
	2. 在`盘符:\你的项目名\quartz\components\Head.tsx`中的`const iconPath = joinSegments(baseDir, "static/favicon.ico")`条目中设置 ico 图标。
	3. 在`盘符:\你的项目名\quartz\components\PageTitle.tsx`中的 return 的`<h1>`标签下的`<a>`标签`<a href={baseDir}><img src="../static/seal.png" width="100" style="vertical-align:middle;"/>{title}</a>`条目中设置网站网面 logo 图片。
6. 发布页面
	我这里尝试了两种方式，见[quartz/docs/hosting.md](https://quartz.jzhao.xyz/hosting)
	- GitHub
	- cloud flare