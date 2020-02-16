---
layout: page
---
### 説明
URLから送られてきた値やフォームで入力した値

### 使い方
    params[:パラメータ名]

### 特徴
* リンクによるパラメータの受け渡し
* フォームによるパラメータの受け渡し

### 例
#### リンクによるパラメータの受け渡し
##### ビュー
        link_to 'ユーザ名', controller: 'users', action: 'show', id: =1
##### コントローラ
        def show
          id = params[:id] # id = 1
        end

#### フォームによるパラメータの受け渡し
##### ビュー
        <% form_for @user do |f| -%>
          名前：<%= f.text_field :name %>
          説明：<%= f.text_area :body %>
        <% end -%>
##### コントローラ
        def create
          name = params[:name]
          body =  params[:body]
        end

#### 配列でパラメータの受け渡し
    xxx[]

#### ハッシュでパラメータの受け渡し
    xxx[aaa]

### その他
#### コントローラ名やアクション名の取得
params[:controller]やparams[:action]で、コントローラ名やアクション名を取得できる