---
layout: page
---
### 説明
クッキーとは、クライアント側に保存されるファイルのこと

### 使い方
    cookies[:クッキー名] = { :key => クッキー情報 }

### オプション

オプション     | 説明              | デフォルト
--------- | --------------- | ------
:value    | クッキーの値          |
:path     | クッキーが有効なパス      |
:domain   | クッキーが有効なドメイン    | 現在のホスト
:expires  | クッキーの有効期限       | /
:secure   | 暗号化通信でのみクッキーを送信 | false
:httponly | HTTPクッキーを有効     | false

### 例
#### クッキーに保存
    cookies[:user_name] = "david"

#### クッキーに配列を保存
    cookies[:lat_lon] = [47.68, -122.37]

#### クッキーにハッシュを保存
    cookies[:login] = { :value => "XJ-122", :expires => 1.hour.from_now }