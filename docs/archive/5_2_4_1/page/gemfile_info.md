---
layout: archive_page
---
### 説明
Railsで使用するGemの依存関係を管理するファイル

### 使い方
    gem ライブラリ名 [, バージョン, オプション]

### バージョン

|バージョン             | 説明
|----------------- | -----------------------------------------------------
|x.x.x             | バージョンを固定
|>= x.x.x          | x.x.x以上のバージョンが必要
|>= x.x.x, < y.y.y | x.x.x以上、y.y.y以下のバージョンが必要
|~> x.0            | x.1からx.9は良いが、メインのバージョンがあがるとは不可。例えば、3.2は良いが、4.0は不可など

### オプション

オプション             | 説明
----------------- | -------------------------------
:branch           | 対象となるブランチ
:group or :groups | 環境(test/development/production)
:git              | gitレポジトリ
:require          | requireするgem
:platforms        | gemを利用するプラットフォーム
:path             | gemファイルのディレクトリを指定

### 例
#### Rails3.2.1で固定
    gem 'rails7, '3.2.1'

#### 最新のRailsを使用
    gem 'rails', git: 'git://github.com/rails/rails.git'

### その他
#### 初めに生成されるファイル例
    source 'https://rubygems.org'

    gem 'rails', '3.2.1'

    gem 'sqlite3'

    gem 'json'

    group :assets do
      gem 'sass-rails',   '~> 3.2.3'
      gem 'coffee-rails', '~> 3.2.1'

      gem 'uglifier', '>= 1.0.3'
    end

#### source
gemで使用するライブラリが置いてあるURL

### 参考サイト
* [Gemfile(5) - A format for describing gem dependencies for Ruby programs](http://gembundler.com/man/gemfile.5.html)