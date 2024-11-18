---
title: "Building a Fast, Modern Blog with Gatsby: A Step-by-Step Guide"
date: "2024-11-10T22:40:32.169Z"
description: This is a custom description for SEO and Open Graph purposes, rather than the default generated excerpt. Simply add a description field to the frontmatter.
---

Regardless of who you are, this book is written for you. And I don’t say
that lightly. There are chapters in this book that cover everything from
hacking the interview process and crafting a killer resume, to creating a
wildly successful blog and building your own personal brand, to being
extremely productive and learning how to deal with burnout, and even
investing in real estate and losing weight. 

This book talk a lot about blogging and how it is important. Specially when you are a freelancer or consultant like me, you‘ll find that a successful blog can bring many clients your way instead of having to go find them by yourself.

Writing articles can also help you become a better developer and communicator because there is a huge work of researching, coding, learning, behind a blog post.

這不是一本教技能的書, 而是一本教思維的書

看過太多軟體工程師說要寫部落格, 是因為


為什麼要寫部落? 
為什麼不用某些平台來寫部落格?
為什麼用gatsby來寫部落格?

因為經歷了「Blogger 網誌被刪除」事件，我計畫將出事的網站搬到自架站，可以避免網站寄人籬下時，需要應付平台的各種合理或不合理規範，不過有相當多問題要解決：

要搬到哪個平台比較適當？如何抉擇各種自架站平台？
能否沿用 Blogger 網址結構(才能不影響 SEO)？
如何克服主機(或是網站託管平台)的流量或其他限制？
能否匯入 Blogger 文章(是否支援 Blogger 匯入格式)？
能否從瀏覽器進入後台？有網路就能進入後台？
能否自動備份網站，預防網站發生任何意外？

這裡面每個主題都相當龐大，且根據自身條件，每個人的解決方案都會不太一樣。為了克服所有困難，等待網站恢復的一個多月主要都在研究這些新的領域。最終我找到的替代方案是 Hexo，本篇會說明為何選擇 Hexo，以及從 Blogger 移轉到 Hexo 的大致流程。

用github托管
先在repository開專案, 用git desktop 下載下來, 把gatsby blog檔案拖過去


---


> 使用 Gatsby 前置環境

1. Node.js (v20.18.0 LTS)
2. Git
3. Gatsby cli (5.13.3)

---

> 安裝 gatsby-cli

```shell
npm install -g gatsby-cli
```

```shell
gatsby new hello-world https://github.com/gatsbyjs/gatsby-starter-hello-world
```

```shell
gatsby new [SITE_DIRECTORY_NAME] [URL_OF_STARTER_GITHUB_REPO]
cd hello-world
gatsby develop
```