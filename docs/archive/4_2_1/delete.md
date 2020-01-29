---
layout: page
---
### 説明
DELETEリクエスト

### 使い方
    delete(URLパターン [, オプション])

### オプション

|オプション                | 説明
|-------------------- | -----------------------------------------------
|:controller, :action | コントローラとアクションを指定。必ずセットで指定
|:to                  | :controller, :actionの短縮形。\#でコントローラとアクションを区切る
|:via                 | HTTPメソッドを指定
|:as                  | ルート名を指定

### 例
    delete 'broccoli', to: 'food#broccoli'

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/78bd18a90992e3da767cfe492f1bc5d63077da8a/activerecord/lib/active_record/relation.rb#L502)