---
title: 街コンジャパンの技術
permalink: /tech/mj
---
# 街コンジャパンの技術

## 技術スタック
- アプリケーション：Ruby on Rails 6, Nuxt 2
- インフラ：EC2, MySQL, Elastic Search, Redis, Memcached

## 主要システムのコード規模
```
サーバーサイド
$ find app -type f -name '*.rb' | xargs wc | tail -1
   58743  147834 2245254 total

クライアントサイド
$ find . -name '*.vue' | xargs wc | tail -1
   43065  111521 1475398 total
$ find . -name '*.js' | xargs wc | tail -1
   20139   48438  605000 total
```

## システムアーキテクチャ
![System Architecture](/assets/images/mj_system_arch.png)
