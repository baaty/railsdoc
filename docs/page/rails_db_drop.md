---
layout: page
---

### 説明

datebase.ymlの設定に従ってデータベースを削除

### 使い方

#### 環境ごと

    $ rails db:drop [RAILS_ENV=環境(development, text, production)]

#### すべて

    $ rails db:drop:all

### 例

#### データベースを削除

    $ rails db:drop

#### production環境のデータベースを削除

    $ rails db:drop RAILS_ENV=production
