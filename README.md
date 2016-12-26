# README兼仕様書


## Installation

```shell
pip install pelican Markdown mdx_linkify mdx_del_ins
```


## 作成中のWebサイトの確認の仕方

ローカル環境にこのリポジトリを`git clone`したあと、outputディレクトリで`python -m pelican.server`して、[http://localhost:8000](http://localhost:8000)にアクセスしてください


## 記事の書き方

1. contentディレクトリ内に記事を作成
2. PyDataOkinawa.github.ioのルートディレクトリで以下のコマンドを実行

    ```shell
    pelican content -o output -s pelicanconf.py
    ```


## Branches
- master  : github-pagesで公開するデータを置くブランチです
- pelican : 開発用のブランチです


## References

[Pelican Docs](http://docs.getpelican.com/en/3.6.3/index.html)

[Configuring a publishing source for GitHub Pages](https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/)

[GPLとは](http://www.weblio.jp/content/GPL)


## Licence
