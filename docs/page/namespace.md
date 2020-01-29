---
layout: page
---
### 特徴
* 名前空間を付与

### 使い方
    namespace モジュール名 [, オプション] do
      ルート定義
    end

### オプション

オプション         | 説明
------------- | ------------
:path         | ルートのパスを指定
:module       | namespaceを指定
:as           | ルート名を指定
:shallow_path | 指定したパラメータを先頭に追加

### 例
#### userにadminの名前空間を付与
    namespace :admin do
      resources :user
    end
    # admin_user_index GET    /admin/user(.:format)          admin/user#index
    #                  POST   /admin/user(.:format)          admin/user#create
    #   new_admin_user GET    /admin/user/new(.:format)      admin/user#new
    #  edit_admin_user GET    /admin/user/:id/edit(.:format) admin/user#edit
    #       admin_user GET    /admin/user/:id(.:format)      admin/user#show
    #                  PUT    /admin/user/:id(.:format)      admin/user#update
    #                  DELETE /admin/user/:id(.:format)      admin/user#destroy

#### sekretと言う名のpathを指定
    namespace :admin, path: "sekret" do
      resources :user
    end
    # admin_user_index GET    /sekret/user(.:format)          admin/user#index
    #                  POST   /sekret/user(.:format)          admin/user#create
    #   new_admin_user GET    /sekret/user/new(.:format)      admin/user#new
    #  edit_admin_user GET    /sekret/user/:id/edit(.:format) admin/user#edit
    #       admin_user GET    /sekret/user/:id(.:format)      admin/user#show
    #                  PUT    /sekret/user/:id(.:format)      admin/user#update
    #                  DELETE /sekret/user/:id(.:format)      admin/user#destroy

#### sekretと言う名のモジュールを指定
    namespace :admin, module: "sekret" do
      resources :user
    end
    # admin_user_index GET    /admin/user(.:format)          sekret/user#index
    #                  POST   /admin/user(.:format)          sekret/user#create
    #   new_admin_user GET    /admin/user/new(.:format)      sekret/user#new
    #  edit_admin_user GET    /admin/user/:id/edit(.:format) sekret/user#edit
    #       admin_user GET    /admin/user/:id(.:format)      sekret/user#show
    #                  PUT    /admin/user/:id(.:format)      sekret/user#update
    #                  DELETE /admin/user/:id(.:format)      sekret/user#destroy

#### sekretと言う名のルート名を指定
    namespace :admin, as: "sekret" do
      resources :user
    end
    # sekret_user_index GET    /admin/user(.:format)          admin/user#index
    #                   POST   /admin/user(.:format)          admin/user#create
    #   new_sekret_user GET    /admin/user/new(.:format)      admin/user#new
    #  edit_sekret_user GET    /admin/user/:id/edit(.:format) admin/user#edit
    #       sekret_user GET    /admin/user/:id(.:format)      admin/user#show
    #                   PUT    /admin/user/:id(.:format)      admin/user#update
    #                   DELETE /admin/user/:id(.:format)      admin/user#destroy

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_dispatch/routing/mapper.rb#L945)