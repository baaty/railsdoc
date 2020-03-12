---
layout: archive_page
---
### 説明
datebase.ymlの設定に従って、データベースを削除

### 使い方
#### 環境ごと
    $ rake db:drop [RAILS_ENV=環境(development, text, production)]

#### すべて
    $ rake db:drop:all

### 例
#### 基本的な使い方
    $ rake db:drop

#### production環境のデータベースを削除
    $ rake db:drop RAILS_ENV=production