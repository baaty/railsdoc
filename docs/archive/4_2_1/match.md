---
layout: page
---
### 説明
アクセス可能なURLを指定することで、HTMLリクエストを処理

### 使い方
    match(URLパターン [, オプション])

### オプション

|オプション                | 説明
|-------------------- | -----------------------------------------------
|:controller, :action | コントローラとアクションを指定。必ずセットで指定
|:to                  | :controller, :actionの短縮形。\#でコントローラとアクションを区切る
|:via                 | HTTPメソッドを指定
|:as                  | ルート名を指定

### 例
#### ルートを定義
    match 'pages/show'
    # pages_show  /pages/show(.:format) pages#show

#### コントローラとアクションを指定
    match "pages", :controller => :pages, :action => :show
    # pages  /pages(.:format) pages#show

#### コントローラとアクションをtoを使った短縮形で指定
    match "pages", :to => 'pages#show'
    # pages  /pages(.:format) pages#show

#### HTTPメソッドを指定
    match "pages/show", :via => :get
    # pages_show GET /pages/show(.:format) pages#show

#### ルート名を指定
    match "pages/show", :as => 'main'
    # main  /pages/show(.:format) pages#show

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f5d2f3fc759ec9a942609ca5b8446e83fdf869b4/actionpack/lib/action_dispatch/routing/mapper.rb#L545)