# README兼仕様書

## Dependency

- Python 3.4
- Pelican 3.7.1.dev0

## Installation & Preparation

    pip install pelican Markdown mdx_linkify mdx_del_ins
    git clone https://github.com/PyDataOkinawa/PyDataOkinawa.github.io.git
    cd PyDataOkinawa.github.io
    git checkout pelican
    git pull origin pelican && git submodule update --init --recursive
    pelican content -o output -s pelicanconf.py

## ローカル環境でWebサイトを確認する方法

上記Installationを実行したあと、生成されたoutputディレクトリ内で`python -m pelican.server`して、ブラウザで[http://localhost:8000](http://localhost:8000)にアクセスしてください


## 記事の書き方

### 1. contentディレクトリ内に記事を作成

#### sample.md

    Title: Ubuntu Install
    Date: 2015-02-18 16:00
    Category: server
    Tags: ubuntu, kernel
    Slug: ubuntu-install
    Author: Matthieu OLIVIER
    Illustration: background.jpg

### 2. ルートディレクトリで以下のコマンドを実行

    pelican content -o output -s pelicanconf.py


## Branches
- master  : github-pages公開用のブランチです
- pelican : 開発用のメインブランチです


## themes

themes/nest-pydataokinawaディレクトリ内のデータは別リポジトリで管理されています([nest-pydataokinawa](https://github.com/PyDataOkinawa/nest-pydataokinawa))


## References

- [Pelican Docs](http://docs.getpelican.com/en/3.6.3/index.html)
- [Configuring a publishing source for GitHub Pages](https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/)
- [GPLとは](http://www.weblio.jp/content/GPL)


## Licence
