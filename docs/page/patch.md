---
layout: page
---
### 説明
PATCHリクエスト

### 使い方
    patch(URLパターン [, オプション])

### オプション

オプション             | 説明
-------------------- | -----------------------------------------------
:controller, :action | コントローラとアクションを指定。必ずセットで指定
:to                  | :controller, :actionの短縮形。\#でコントローラとアクションを区切る
:via                 | HTTPメソッドを指定
:as                  | ルート名に指定する別名

### 例
#### PATCHリクエスト
    patch 'bacon', to: 'food#bacon'

#### コントローラとアクションを指定
    patch 'follow' ,:controller =>'discussion_followers',:action=>'create'

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_dispatch/routing/mapper.rb#L727)