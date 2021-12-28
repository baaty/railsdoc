---
layout: page
---

### 説明

指定した条件のレコードを削除  
dependentが設定されている場合は関連付けられたモデルも削除

### 使い方

    モデル.destroy(ID)

### 例

#### 指定した条件のレコードを削除  

    Todo.destroy(1)

#### 複数指定

    Todo.destroy([1,2,3])

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/persistence.rb#L448)
