---
layout: archive_page
---
### 説明
フィクスチャファイルを使って、データベースにテストデータを挿入

### 使い方
    $ rake db:fixtures:load [FIXTURES=フィクスチャファイル名 RAILS_ENV=環境]

### 例
#### 基本形(オプションなし)
    $ rake db:fixtures:load