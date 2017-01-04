# README兼仕様書

## Dependency

- Python 3.4
- Pelican 3.7.1.dev0

## Installation

```shell
pip install pelican Markdown mdx_linkify mdx_del_ins
git clone https://github.com/PyDataOkinawa/PyDataOkinawa.github.io.git
cd themes/nest-pydtaokinawa
git submodule init
git submodule update
```


## 作成中のWebサイトの確認の仕方

上記のコマンドを実行したあと、outputディレクトリで`python -m pelican.server`して、[http://localhost:8000](http://localhost:8000)にアクセスしてください


## 記事の書き方

1. contentディレクトリ内に記事を作成
2. PyDataOkinawa.github.ioのルートディレクトリで以下のコマンドを実行

    ```shell
    pelican content -o output -s pelicanconf.py
    ```


## Branches
- master  : github-pages公開用のブランチです
- pelican : 開発用のメインブランチです


## themes

thmes/nest-pydataokinawaディレクトリ内のデータは別のリポジトリで管理されています([nest-pydataokinawa](https://github.com/PyDataOkinawa/nest-pydataokinawa))


## References

- [Pelican Docs](http://docs.getpelican.com/en/3.6.3/index.html)
- [Configuring a publishing source for GitHub Pages](https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/)
- [GPLとは](http://www.weblio.jp/content/GPL)


## Licence
