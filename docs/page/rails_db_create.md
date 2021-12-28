---
layout: page
---

### 説明

datebase.ymlの設定に従ってデータベースを作成

### 使い方

#### 環境ごと

    $ rails db:create [RAILS_ENV=環境(development, text, production)]

#### すべて

    $ rails db:create:all

### 例

#### データベースを作成

    $ rails db:create

#### production環境

    $ rails db:create RAILS_ENV=production
