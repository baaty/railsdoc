---
layout: page
---
### 説明
モデルクラス名からテーブル名へ変換
「config/initializers/inflections.rb」に定義を追加することによって追加

### 使い方
    <モデルクラス名>.tableize

### 例
#### 「Page」を変換
    "Page".tableize
    # "pages"

#### 「AdminUser」を変換
    "AdminUser".tableize
    # "admin_users"