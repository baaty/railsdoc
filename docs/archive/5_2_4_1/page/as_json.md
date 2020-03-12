---
layout: archive_page
---
### 説明
モデルをハッシュ形式のJSONに変換

### 使い方
    モデル.as_json([オプション])

### オプション

オプション | 説明 | デフォルト値
---- | ---- | ----
:root | ノード名を含める | false
:only | 取得する要素を指定 |
:except | 取得しない要素を指定 |
:methods | メソッドの呼び出し結果を含める |
:include | 関連付け |

### 例
#### モデルをハッシュ形式のJSONに変換
    user.as_json
    # {id: 1, name: "Konata Izumi", age: 16, created_at: "2006-08-01T17:27:133.000Z", awesome: true}

#### ノード名を含める
    user.as_json(root: true)
    # => { "user" => { "id" => 1, "age" => 16, "created_at" => "2006-08-01T17:27:13.000Z", "awesome" => true } }

#### 取得する要素を指定
    user.as_json(only: [:id, :age])
    # => { "id" => 1, "age" => 16 }

#### 取得しない要素を指定
    user.as_json(except: [:id, :created_at, :name])
    # => { "age" => 16, "awesome" => true }

#### メソッドを指定
    user.as_json(methods: :permalink)
    # => { "id" => 1, "name" => "Konata Izumi", "age" => 16, "created_at" => "2006-08-01T17:27:13.000Z", "awesome" => true, "permalink" => "1-konata-izumi" }

#### 関連付け
    user.as_json(include: :posts)
    # => { "id" => 1, "name" => "Konata Izumi", "age" => 16, "created_at" => "2006-08-01T17:27:13.000Z", "awesome" => true, "posts" => [ { "id" => 1, "author_id" => 1, "title" => "Welcome to the weblog" }, { "id" => 2, "author_id" => 1, "title" => "So I was thinking" } ] }

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activemodel/lib/active_model/serializers/json.rb#L89)