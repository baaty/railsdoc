---
layout: archive_page
---
### 説明
設定されているルーティングの内容を確認

### 使い方
    $ rake routes

### 例
#### ルーティングの内容を確認
    $ rake routes
      Prefix Verb   URI Pattern               Controller#Action
       xxxes GET    /xxxes(.:format)          xxxes#index
             POST   /xxxes(.:format)          xxxes#create
     new_xxx GET    /xxxes/new(.:format)      xxxes#new
    edit_xxx GET    /xxxes/:id/edit(.:format) xxxes#edit
         xxx GET    /xxxes/:id(.:format)      xxxes#show
             PATCH  /xxxes/:id(.:format)      xxxes#update
             PUT    /xxxes/:id(.:format)      xxxes#update
             DELETE /xxxes/:id(.:format)      xxxes#destroy