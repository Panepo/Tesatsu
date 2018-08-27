---
title: Download Box
categories:
  - 程設
tags:
  - 程設
date: 2018-08-27 17:26:37
---
今天在寫 js 的時候碰到一個有趣的東西, 平常瀏覽網頁的下載按鈕, 如果在按下後需要下載的資料才產生出來的話, 要怎麼做呢?

{% codeblock %}
let downloadAnchorNode = document.createElement('a')
downloadAnchorNode.setAttribute('href', 'data:' + data)
downloadAnchorNode.setAttribute('download', 'faceData.json')
downloadAnchorNode.click()
downloadAnchorNode.remove()
{% endcodeblock %}

就憑空生出一個超連結的 element, 接著把產生出來的資料連結過去, 然後幫你按下那超連結, 再把超連結刪掉! 一切都那麼自然看不到過程 XD
