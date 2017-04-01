# README兼仕様書

## Dependency

- Python 3.4
- Pelican 3.7.1.dev0

## Installation & Preparation

    pip install pelican Markdown mdx_linkify mdx_del_ins ghp-import
    git clone https://github.com/PyDataOkinawa/PyDataOkinawa.github.io.git
    cd PyDataOkinawa.github.io
    git checkout pelican
    git submodule update --init --recursive
    pelican content -o output -s pelicanconf.py

### git submodule update --init --recursiveでエラーが出てしまう場合

先程クローンしてきたpyDataOkinawa.ioのディレクトリに.gitmoduleというファイルがありますのでそちらを編集してください
    
#### 編集前

    [submodule "themes/nest-pydataokinawa"]
        path = themes/nest-pydataokinawa
        url = git@github.com:PyDataOkinawa/nest-pydataokinawa.git

#### 編集後

    [submodule "themes/nest-pydataokinawa"]
        path = themes/nest-pydataokinawa
        url = https://www.github.com/PyDataOkinawa/nest-pydataokinawa.git

編集が終わったら以下のコマンドを実行してください

    git submodule sync
    git submodule update --init --recursive
    pelican content -o output -s pelicanconf.py

## ローカル環境でWebサイトを確認する方法

    cd output
    python -m pelican.server

上記コマンドを実行後、http://localhost:8000](http://localhost:8000)にアクセスしてください


## ブログ記事の書き方

### 1. 記事を書く前にリモートリポジトリからデータの差分を取得

    git pull origin pelican && git submodule update --init --recursive

### 2. content/articlesディレクトリ内に記事を作成

    cp template/sample.md content/YOUR_ARTICLE_TITLE.md

自分の好きなエディタで`content/YOUR_ARTICLE_TITLE.md`を編集してください

### 3. ルートディレクトリで以下のコマンドを実行

    pelican content -o output -s pelicanconf.py

### 4. リモートリポジトリにPushしてサイトを更新

※このコマンドを実行するとすぐ公開しているHPが更新されますので注意してください

    ghp-import output && git push origin gh-pages:master pelican:pelican

## Branches
- master  : 公開用のブランチ
- pelican : ソースを保存するブランチ

## themes

themes/nest-pydataokinawaディレクトリ内のデータは別リポジトリで管理されています([nest-pydataokinawa](https://github.com/PyDataOkinawa/nest-pydataokinawa))

## References

- [Pelican Docs](http://docs.getpelican.com/en/3.6.3/index.html)
- [Configuring a publishing source for GitHub Pages](https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/)

## Licence
