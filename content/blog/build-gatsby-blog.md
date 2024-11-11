---
title: "Building a Fast, Modern Blog with Gatsby: A Step-by-Step Guide"
date: "2024-11-10T22:40:32.169Z"
description: This is a custom description for SEO and Open Graph purposes, rather than the default generated excerpt. Simply add a description field to the frontmatter.
---

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