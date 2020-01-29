---
layout: page
---
1.  作業ディレクトリの作成

        $ mkdir rails
        $ cd rails

2.  アプリケーション作成

        $ rails new demo

3.  ディレクトリ移動

        $ cd demo

4.  必要なgemのインストール

        $ bundle install

5.  データベースの設定

        $ vi config/database.yml

6.  データベースの作成

        $ rake db:create

7.  ジェネレータ

        $ rails generate controller Say Hello goodbye

8.  テーブル作成

        $ rake db:migrate

9.  サーバ起動

        $ rails server