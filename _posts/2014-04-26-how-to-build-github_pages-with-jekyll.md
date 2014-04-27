---
layout: post
title:  "jekyll + GitHub Pagesでブログ構築"
date:   2014-04-26 10:14:00
categories: website
tags: jekyll GitHub-Pages
---

元々普通にhtmlで書いていたユーザーページを、jekyllで簡単に更新できるようにしました。

- [Github Pages について整理しておきます][1]
- [Jekyllいつやるの？ジキやルの？今でしょ！][2]

を参考にしました。丁寧な解説記事に感謝。

# jekyllのインストールとひな形作成メモ
※ jekyllをローカルインストールしたかったのでjekyll newあたりが上の記事と違います

```sh 
$ mkdir myblog
$ cd myblog
$ rbenv local 2.1.1 #プロジェクト内のrubyのバージョンを2.1.1に指定
$ bundle init
$ echo 'gem "jekyll"' >> Gemfile
$ bundle install --path vendor/bundle
$ bundle exec jekyll new . --force #カレントディレクトリにブログのひな形を作成
$ bundle exec jekyll server
```

[1]: http://blog.eiel.info/blog/2013/02/17/github-pages/
[2]: http://melborne.github.io/2013/05/20/now-the-time-to-start-jekyll
