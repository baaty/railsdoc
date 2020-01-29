---
layout: page
---
### 説明
マイグレーションの履歴を表示

### 使い方
    $ rake db:migrate:status [RAILS_ENV=環境(development, text, production)]

### 例
#### 基本形(オプションなし)
    $ rake db:migrate:status

     Status   Migration ID    Migration Name
    --------------------------------------------------
       up     20110521181506  Create pages
       up     20110521182915  Create categories
       up     20110703120321  Add position to pages
       up     20110716180121  Add position to categories
      down  20110724110158  Add english name to category