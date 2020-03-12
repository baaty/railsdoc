---
layout: archive_page
---
### 説明
DELETEリクエスト

### 使い方
    delete(パス [, オプション])

### オプション

|オプション                | 説明
|-------------------- | -----------------------------------------------
|:controller, :action | コントローラとアクションを指定。必ずセットで指定
|:to                  | :controller, :actionの短縮形。\#でコントローラとアクションを区切る
|:via                 | HTTPメソッドを指定
|:as                  | ルート名に使用する別名

### 例
#### DELETEリクエスト
    delete 'broccoli', to: 'food#broccoli'

#### ルート名に使用する別名を指定
    delete '/delete/:id', action: 'destroy', as: 'destroy_user'

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionpack/lib/action_dispatch/routing/mapper.rb#L735)