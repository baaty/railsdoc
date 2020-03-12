---
layout: archive_page
---
1. 作業ディレクトリの作成

        $ mkdir rails
        $ cd rails

2. アプリケーション作成

        $ rails new demo

3. ディレクトリ移動

        $ cd demo

4. ジェネレータ

        $ rails generate controller Welcome index

5. ルーティング

        $ vim config/routes.rb
        Rails.application.routes.draw do
          get 'welcome/index'
          root 'welcome#index'
        end

6. サーバ起動

        $ rails server
        # http://localhost:3000にアクセス