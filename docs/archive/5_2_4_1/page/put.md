---
layout: archive_page
---
### 説明
PUTリクエスト

### 使い方
    put(URLパターン [, オプション])

### オプション

オプション             | 説明
-------------------- | -----------------------------------------------
:controller, :action | コントローラとアクションを指定。必ずセットで指定
:to                  | :controller, :actionの短縮形。\#でコントローラとアクションを区切る
:via                 | HTTPメソッドを指定
:as                  | ルート名に使用する別名

### 例
#### PUTリクエスト
    put 'bacon', to: 'food#bacon'

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_dispatch/testing/integration.rb#L35)