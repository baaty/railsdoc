---
layout: page
---
### 説明
RESTfulなURLを自動生成

### 使い方
    resources :リソース名 [, オプション]

### 生成されるルート

URL                      | アクション   | HTTPメソッド | 説明
------------------------ | ------- | -------- | -------
/XXXs(.:format)          | index   | GET      | 一覧画面を生成
/XXXs/:id(.:format)      | show    | GET      | 詳細画面を生成
/XXXs/new(.:format)      | new     | GET      | 登録画面を生成
/XXXs(.:format)          | create  | POST     | 登録処理
/XXXs/:id/edit(.:format) | edit    | GET      | 編集画面を生成
/XXXs/:id(.:format)      | update  | PUT      | 更新処理
/XXXs/:id(.:format)      | destroy | DELETE   | 削除処理

### 生成されるパス

パス                 | URL               | 戻り値
------------------ | ----------------- | --------------
XXXs_path          | XXXs_url          | /XXXs
XXX_path(:id)      | XXX_url(:id)      | /XXXs/:id
new_XXX_path       | new_XXX_url       | /XXXs/new
edit_XXX_path(:id) | edit_XXX_url(:id) | /XXXs/:id/edit

### オプション

オプション           | 説明
--------------- | -------------------------------------------------------------------------------------------------------------------------------------
:as             | ルート名に利用する別名
:controller     | コントローラを指定
:path_names     | 指定したアクションのみ名前の変更
:path           | URLを書き換える
:only           | 生成されるURLを絞り込む
:except         | 指定したURLは生成しない
:shallow        | Generates shallow routes for nested resource(s). When placed on a parent resource, generates shallow routes for all nested resources.
:shallow_path   | Prefixes nested shallow routes with the specified path.
:shallow_prefix | Prefixes nested shallow route names with specified prefix.
:format         | Allows you to specify the default value for optional format segment or disable it by supplying false.

### 例
#### RESTfulなURLを自動生成
    resources :pages
    #     pages GET    /pages(.:format)          pages#index
    #           POST   /pages(.:format)          pages#create
    #  new_page GET    /pages/new(.:format)      pages#new
    # edit_page GET    /pages/:id/edit(.:format) pages#edit
    #      page GET    /pages/:id(.:format)      pages#show
    #           PUT    /pages/:id(.:format)      pages#update
    #           DELETE /pages/:id(.:format)      pages#destroy

#### ルート名に使用する名前をmainにする
    resources :pages, :as => :main
    # main_index GET    /pages(.:format)          pages#index
    #            POST   /pages(.:format)          pages#create
    #   new_main GET    /pages/new(.:format)      pages#new
    #  edit_main GET    /pages/:id/edit(.:format) pages#edit
    #       main GET    /pages/:id(.:format)      pages#show
    #            PUT    /pages/:id(.:format)      pages#update
    #            DELETE /pages/:id(.:format)      pages#destroy

#### 処理するコントローラを指定
    resources :pages, :controller => :mains
    #     pages GET    /pages(.:format)          mains#index
    #           POST   /pages(.:format)          mains#create
    #  new_page GET    /pages/new(.:format)      mains#new
    # edit_page GET    /pages/:id/edit(.:format) mains#edit
    #      page GET    /pages/:id(.:format)      mains#show
    #           PUT    /pages/:id(.:format)      mains#update
    #           DELETE /pages/:id(.:format)      mains#destroy

#### URLを置き換える
    resources "pages", :path => 'admin/page'
    #     pages GET    /admin/page(.:format)          pages#index
    #           POST   /admin/page(.:format)          pages#create
    #  new_page GET    /admin/page/new(.:format)      pages#new
    # edit_page GET    /admin/page/:id/edit(.:format) pages#edit
    #      page GET    /admin/page/:id(.:format)      pages#show
    #           PUT    /admin/page/:id(.:format)      pages#update
    #           DELETE /admin/page/:id(.:format)      pages#destroy

#### 作成されるURLを絞り込む
    resources :pages, :only => [:index]
    # pages GET /pages(.:format) pages#index

#### 作成しないURLを指定
    resources :pages, :except => [:index, :show]
    #     pages POST   /pages(.:format)          pages#create
    #  new_page GET    /pages/new(.:format)      pages#new
    # edit_page GET    /pages/:id/edit(.:format) pages#edit
    #      page PUT    /pages/:id(.:format)      pages#update
    #           DELETE /pages/:id(.:format)      pages#destroy

#### コントローラにnamespaceを不要
    resources :pages, :module => :main
    #     pages GET    /pages(.:format)          main/pages#index
    #           POST   /pages(.:format)          main/pages#create
    #  new_page GET    /pages/new(.:format)      main/pages#new
    # edit_page GET    /pages/:id/edit(.:format) main/pages#edit
    #      page GET    /pages/:id(.:format)      main/pages#show
    #           PUT    /pages/:id(.:format)      main/pages#update
    #           DELETE /pages/:id(.:format)      main/pages#destroy

#### 制限を付ける
    resources :users, :constraints => {:title => /[a-z]{1,15}/}
    #     users GET    /users(.:format)          users#index {:title=>/[a-z]{1,15}/}
    #           POST   /users(.:format)          users#create {:title=>/[a-z]{1,15}/}
    #  new_user GET    /users/new(.:format)      users#new {:title=>/[a-z]{1,15}/}
    # edit_user GET    /users/:id/edit(.:format) users#edit {:title=>/[a-z]{1,15}/}
    #      user GET    /users/:id(.:format)      users#show {:title=>/[a-z]{1,15}/}
    #           PUT    /users/:id(.:format)      users#update {:title=>/[a-z]{1,15}/}
    #           DELETE /users/:id(.:format)      users#destroy {:title=>/[a-z]{1,15}/}

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f5d2f3fc759ec9a942609ca5b8446e83fdf869b4/actionpack/lib/action_dispatch/routing/mapper.rb#L1348)