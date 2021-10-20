---
title: CoupLink の技術
permalink: /tech/cl
---
# CoupLink の技術

## 技術スタック
- アプリケーション：Ruby on Rails 5.2, Vue.js 3.2
- インフラ：EC2, MySQL, Redis, Memcached

iOSアプリ、Androidアプリ、Webアプリを提供しています。ユーザの大多数は iOSアプリ、Androidアプリを利用しています。ネイティブアプリとしてストアにリリースしていますが、決済や通知などの一部を除いて、中身は Vue.js で作られた WebView です。Vue.js を駆使して、Webの技術でネイティブに近い操作性を実現しています。

## コード規模
```
サーバーサイド
$ find app -type f -name '*.rb' | xargs wc | tail -1
   37466   85161 1203268 total

クライアントサイド
$ find . -name '*.vue' | xargs wc | tail -1
   62385  153509 1911983 total
$ find . -name '*.js' | xargs wc | tail -1
    7280   25805  332820 total
$ find . -name '*.swift' | xargs wc | tail -1
    5239   15412  189017 total
$ find . -name '*.java' | xargs wc | tail -1
    5872   17473  220079 total

モデル数
$ ls app/models/*.rb | wc
     139     139    4055
```

## コードの「年齢」
現在のシステムは v2 と呼ばれるもので、2018年8月にリリースしたものです。2018年1月に入社したメンバーが、技術的負債に耐えかねてリニューアルを決断し、一人で大半を書きました。まだ老朽化も技術的負債も無いため、しばらくはこのコードベースを使い続ける予定です。
