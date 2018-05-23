---
title: Deployment
date: 2018-05-23 09:46:32
categories: [手札, 程設]
tags: [手札, 程設]
---
這篇為使用 Travis CI 自動佈署 web application 到 Github pages 的方法來做個紀錄.

### Travis CI 設定

- 申請 Tarvis CI 帳號
- 將 github 資料庫和 travis ci 做連結
- 增加 .travis.yml 檔案至 Github 資料庫

### .travis.yml 設定

- 首先要準備一組 personal access token 給 Travis CI. 到 Github 的 settings 頁面下的 personal access token 產生一組有 repo 權限的 token.

- 接下來安裝官方提供的 ruby 套件 travis command line tool.
  `gem install travis`
  
  使用命令列工具登入 GitHub
  `travis login`

  使用命令列工具將剛產生出來的 token 加密並寫入 Travis CI 設定檔
  `travis encrypt 'GIT_NAME="<Github ID>" GIT_EMAIL=<Github email> 'GH_TOKEN=<Token>' --add`
  
- 再來是讓 Travis CI 自動 build, 並讓生成的檔案往 Github 資料庫中的 gh-pages 分支 push, 這些都寫在設定檔中的 install 和 script 區塊.

最後文件檔的配置如下:

{% codeblock .travis.yml %}
language: node_js

node_js:
  - "8.9.1"

env:
  global:
    secure: XN7bTWNHQyFk9Mq656K9iYCp3apSwVECA1PGQQUnrdpjfZXDTvDlxhbN65euShbH2tsKxPRnXq47wzkKw38NS2TonrF05cUiA4O49sd8Nifh3YJe9ynx9NfmLjq22qpP0Ul9+d9NFGIkiactMC22ho8KcEYXs9KEx8r4gytkdvNC0dqYzmI9bPx9TNg5k1MmAKwzwB/Sy2MVudhJGUPMMhDD8i2zUS/ollrnuK6CG+UGu39/2/IyEtrcQZ5/jm6m4Bo+ofnOro8+9x/y/RlzGGjsjvBDVl7Jodd6Nuu4FLQjsD6fOzrV+mgFZKU+nE4/8Qc9HiM2cT7DqWMOy05Lx2XqN48/gerv7qPeglEIqIhHGmz0poAgc0TCp552Ys8TFMhpbuUvBeIxxbzCjFD5hgTpgFHnVo+F7PEOTEBapRnK2H+5PNRgJsT1vtsQw1wXf3VxwUHsa7F+UO2sD6QpJGG1xJZWGx4eSLWVHxLEfCr76vEWXadoNtZ8VkjInuYMtllSf7J8nECSoCJKYarYlXtiGgzHhtItLPmH9QMHtgc2RNyliL6z4zc8EeAuKDT0lZYYpyvplzHbgSyidLxi3X/wsx4cwjU3n1oag8A9JFK3iY745ctXv3SjhWrPPsQUpuVkZVQwnLxU2geTVbYzNFBs8cL2h8I6XIFRPVgPkA4=
    
before_install:
  - export TZ=Asia/Taipei

install:
  - npm install
  - npm install -g hexo-cli

script:
  # Set Git config
  - git config --global user.name "$GIT_NAME"
  - git config --global user.email "$GIT_EMAIL"
  - git config --global push.default simple
  - git clone --depth 1 --branch gh-pages https://$GH_TOKEN@github.com/Panepo/Tesatsu public
  # Generate static pages
  - hexo generate
  - cd public
  - git add -A .
  - MESSAGE=`date +\ %Y-%m-%d\ %H:%M:%S`
  - git commit -m "Travis CI auto deploy:$MESSAGE"
  - git push --quiet
{% endcodeblock %}