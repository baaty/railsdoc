---
layout: page
---
### 説明
datebase.ymlの設定に従って、データベースを作製

### 使い方
#### 環境ごと
    $ rake db:create [RAILS_ENV=環境(development, text, production)]

#### すべて
    $ rake db:create:all

### 例
#### 基本形(オプションなし)
    $ rake db:create