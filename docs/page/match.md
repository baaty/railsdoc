---
layout: page
---
### 説明
アクセス可能なURLを指定することで、HTMLリクエストを処理

### 使い方
    match(URLパターン [, オプション])

### オプション

オプション             | 説明
-------------------- | -----------------------------------------------
:controller, :action | コントローラとアクションを指定。必ずセットで指定
:to                  | :controller, :actionの短縮形。\#でコントローラとアクションを区切る
:param               |
:path                |
:module              |
:via                 | HTTPメソッドを指定
:as                  | ルート名を指定

### 例
#### ルートを定義
    match 'pages/show'
    # pages_show  /pages/show(.:format) pages#show

#### コントローラとアクションを指定
    match "pages", controller: :pages, action: :show
    # pages  /pages(.:format) pages#show

#### コントローラとアクションをtoを使った短縮形で指定
    match "pages", to: 'pages#show'
    # pages  /pages(.:format) pages#show

#### HTTPメソッドを指定
    match "pages/show", via: :get
    # pages_show GET /pages/show(.:format) pages#show

#### ルート名を指定
    match "pages/show", as: 'main'
    # main  /pages/show(.:format) pages#show

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_dispatch/routing/mapper.rb#L590)