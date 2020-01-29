---
layout: page
---
### 説明
モデルをハッシュに変換

### 使い方
    モデル.as_json([オプション])

### 例
    user.as_json
    # {id: 1, name: "Konata Izumi", age: 16, created_at: "2006-08-01T17:27:133.000Z", awesome: true}

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activemodel/lib/active_model/serializers/json.rb#L89)