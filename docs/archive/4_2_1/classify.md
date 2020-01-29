---
layout: page
---
### 説明
テーブル名からモデルクラス名へ変換
「config/initializers/inflections.rb」に定義を追加することによって可能

### 使い方
    <テーブル名>.classify

### 例
#### 「people」を変換
    "people".classify
    # "Person"