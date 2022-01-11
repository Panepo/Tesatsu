---
title: PileBunkter-ts
categories:
  - JS
tags:
  - 吟遊
  - 程設
date: 2019-03-06 16:16:26
---
過年期間太鹹, 想說來學個 typescript 就把計算機整個重新改寫了一遍.

連結網址{% link 在此 https://panepo.github.io/PileBunker-ts/ %}

UI 也稍微改過, 原先上面亂七八糟的輸入欄位現在分成三組並可折疊
https://raw.githubusercontent.com/Panepo/PileBunker-ts/master/doc/demo1.png

原先選擇城娘攻擊係數的地方, 點選攻擊成長係數% 那就會彈出
https://raw.githubusercontent.com/Panepo/PileBunker-ts/master/doc/demo2.png

下面表格的地方, 部分資訊改放成在點擊武器名稱時跳出的小視窗裡面
https://raw.githubusercontent.com/Panepo/PileBunker-ts/master/doc/demo3.png

另外新增了兜的數量以及耐久的設定, 用於計算總擊破時間.
擊破時間不會和 dps 呈正相關, 畢竟除了鈴鐺外都是算攻擊幾次,
所以溢傷嚴重的三連鐵炮在這項目會表現得很差勁
目前鎚子, 槍, 大砲, 鈴鐺和歌舞在計算上是攻擊全體, 所以數量一多表現會很優異.

目前尚未實裝部分
1. 兜的選擇, 先到非公開老師那邊查吧
2. 兜的各種雜七雜八傷害減免, 像是大鳥兜的遠隔物理ダメージ50%軽減
   馬面的近接ダメージ30%軽減 牛頭的遠隔ダメージ30%軽減
   總覺得裝上去又會讓輸入欄位變得一大堆亂七八糟.. orz

3. 各種 debuff 賦予的武器, 效果不會填上, 像是
   未来ガジェット5号機: 敵の攻撃と防御を10%下げる
   (防禦無視內建的武器有實裝計算, 像是 ヴァリス)

有甚麼建議或是錯誤麻煩請留言或是寫信給我
由於有用到 app 狀態持久化的 library, 會儲存一些資訊在各位電腦上
用於開啟網頁時恢復上次的瀏覽狀態.
在我進行大改版的時候會因為資料格式錯誤而跳 error,
這時候只要去瀏覽器刪除 panepo.github.io 底下的暫存資料即可

對程式有興趣的鄉民, 程式碼{% link 在這 https://github.com/Panepo/PileBunker-ts %}

用 typescript, create react app 等寫成歡迎指教

謝謝
