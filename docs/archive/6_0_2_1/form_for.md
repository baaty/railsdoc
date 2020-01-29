---
layout: page
---
### 説明
汎用的なフォームを生成

### 使い方
    form_for(モデルオブジェクト [, オプション]) do |f|
      フォームの本体
    end

### オプション

オプション      | 説明
---------- | --------
:url       | フォームの送信先
:namespace | 名前空間の設定
:html      | タグの属性

### 例
#### 基本形(オプションなし)
    <%= form_for(@user) do |f| %>
    <% end %>
    # <form action="/users" class="new_user" id="new_user" method="post">
    # </form>

#### urlオプション
    <%= form_for @user, url: {action: 'update'} do |f| %>
    <% end %>
    # <form action="/users/update" class="new_user" id="new_user" method="post">
    # </form>

#### htmlオプション
    <%= form_for(@user, html: {multipart: true}) do |f| %>
    <% end %>
    # <form action="/users" class="new_user" enctype="multipart/form-data" id="new_user" method="post">
    # </form>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L430)