---
layout: page
---

### 説明

このクエリを識別できるたキャッシュキーを取得

### 使い方

    モデル.cache_key(タイムスタンプカラム='updated_at')

### 例

#### キャッシュキーを取得

    Product.where("name like ?", "%Cosmic Encounter%").cache_key

#### タイムスタンプカラムを指定

    Product.where("name like ?", "%Game%").cache_key(:last_reviewed_at)

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation.rb#L320)
