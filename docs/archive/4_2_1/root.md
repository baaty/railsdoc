---
layout: page
---
### 説明
ルート(/)のURLを指定

### 使い方
    root([オプション])

### オプション

オプション                | 説明
-------------------- | -----------------------------------------------
:controller, :action | コントローラとアクションを指定。必ずセットで指定
:to                  | :controller, :actionの短縮形。\#でコントローラとアクションを区切る
:via                 | HTTPメソッドを指定
:as                  | ルート名を指定

### 注意点
* /public/以下のファイルが優先して認識するため、デフォルトで置いてあるindex.htmlは削除してください

### 例
#### pagesコントローラとindexアクションをrootに指定
    root :controller => 'pages', :action => 'index'
    # root  / pages#index

#### コントローラとアクションをtoを使った省略形で記述
    root :to => 'pages#index'
    # root  / pages#index

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f5d2f3fc759ec9a942609ca5b8446e83fdf869b4/actionpack/lib/action_dispatch/routing/mapper.rb#L386)