---
layout: page
---
### 説明
マイグレーションを前のバージョンに戻す

### 使い方
    $ rake db:rollback

### 例
#### 基本形(オプションなし)
    $ rake db:rollback

#### ３つ前にロールバック
    $ rake db:rollback STEP=3