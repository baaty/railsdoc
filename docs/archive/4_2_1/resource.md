---
layout: page
---
### 説明
RESTfulなURLを自動生成

### 使い方
    resource(リソース名 [, オプション])

### 生成されるルート

URL                 | アクション   | HTTPメソッド | 説明
------------------- | ------- | -------- | -------
/XXX(.:format)      | show    | GET      | 詳細画面を生成
/XXX/new(.:format)  | new     | GET      | 登録画面を生成
/XXX(.:format)      | create  | POST     | 登録処理
/XXX/edit(.:format) | edit    | GET      | 編集画面を生成
/XXX(.:format)      | update  | PUT      | 更新処理
/XXX(.:format)      | destroy | DELETE   | 削除処理

### 生成されるパス

パス            | URL          | 戻り値
------------- | ------------ | ---------
XXX_path      | XXX_url      | /XXX
new_XXX_path  | new_XXX_url  | /XXX/new
edit_XXX_path | edit_XXX_url | /XXX/edit

### オプション

オプション        | 説明
------------ | -------------
:as          | ルート名に利用する別名
:controller  | コントローラを指定
:path        | URLを書き換える
:only        | 生成されるURLを絞り込む
:except      | 指定したURLは生成しない
:module      | namespaceを付与
:constraints | 制限を付ける

### 例
#### 単一のリソースを定義
    resource :page
    #      page POST   /page(.:format)      pages#create
    #  new_page GET    /page/new(.:format)  pages#new
    # edit_page GET    /page/edit(.:format) pages#edit
    #           GET    /page(.:format)      pages#show
    #           PUT    /page(.:format)      pages#update
    #           DELETE /page(.:format)      pages#destroy

#### ルート名に使用する名前
    resource :page, :as => :main
    #      main POST   /page(.:format)      pages#create
    #  new_main GET    /page/new(.:format)  pages#new
    # edit_main GET    /page/edit(.:format) pages#edit
    #           GET    /page(.:format)      pages#show
    #           PUT    /page(.:format)      pages#update
    #           DELETE /page(.:format)      pages#destroy

#### 処理するコントローラを指定
    resource :page, :controller => :main
    #      page POST   /page(.:format)      main#create
    #  new_page GET    /page/new(.:format)  main#new
    # edit_page GET    /page/edit(.:format) main#edit
    #           GET    /page(.:format)      main#show
    #           PUT    /page(.:format)      main#update
    #           DELETE /page(.:format)      main#destroy

#### URLを置き換える
    resource :page, :path => 'admin/page'
    #      page POST   /admin/page(.:format)      pages#create
    #  new_page GET    /admin/page/new(.:format)  pages#new
    # edit_page GET    /admin/page/edit(.:format) pages#edit
    #           GET    /admin/page(.:format)      pages#show
    #           PUT    /admin/page(.:format)      pages#update
    #           DELETE /admin/page(.:format)      pages#destroy

#### 作成されるURLを絞り込む
    resource :page, :only => [:show]
    # page GET /page(.:format) pages#show

#### 作成しないURLを指定
    resource :page, :except => [:create, :new]
    # edit_page GET    /page/edit(.:format) pages#edit
    #      page GET    /page(.:format)      pages#show
    #           PUT    /page(.:format)      pages#update
    #           DELETE /page(.:format)      pages#destroy

#### コントローラにnamespaceを不要
    resource :page, :module => :admin
    #      page POST   /page(.:format)      admin/pages#create
    #  new_page GET    /page/new(.:format)  admin/pages#new
    # edit_page GET    /page/edit(.:format) admin/pages#edit
    #           GET    /page(.:format)      admin/pages#show
    #           PUT    /page(.:format)      admin/pages#update
    #           DELETE /page(.:format)      admin/pages#destroy

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f5d2f3fc759ec9a942609ca5b8446e83fdf869b4/actionpack/lib/action_dispatch/routing/mapper.rb#L1190)