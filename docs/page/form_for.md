---
layout: page
---
### 説明
特定のモデルに特化したフォームを生成  
form_withの利用を推奨(Rails5.1以降はform_forとform_tagはform_withに統合されたため)

### 使い方
    form_for(モデルオブジェクト [, オプション]) do |f|
      フォームの本体
    end

### オプション

オプション               | 説明                                  | デフォルト値
--------------------|---------------------------------------|-------
:as                 | ハッシュのキー名前                           |
:url                | フォームの送信先                           |
:namespace          | 名前空間の設定                         |
:method             | メソッド(get, post, patch, put, deleteなど) |
:authenticity_token | 認証トークン                              |
:remote             | JavaScriptを使うか                       | false
:enforce_utf8       | utf8用の非表示用を出力するか?              | true
:html               | タグの属性                               |
:format             | フォーマット |

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

#### HTML属性を指定
    <%= form_for(@user, html: {multipart: true}) do |f| %>
    <% end %>
    # <form action="/users" class="new_user" enctype="multipart/form-data" id="new_user" method="post">
    # </form>

#### ハッシュのキー名を変更
    <%= form_for(@person, as: :client) do |f| %>
    <% end %>
    # params[:client]で取得できるようになる

#### フォーマット指定
    <%= form_for(@post, format: :json) do |f| %>
    <% end %>

#### JavaScriptを使用
    <%= form_for(@post, remote: true) do |f| %>
    <% end %>
    # <form action='http://www.example.com' method='post' data-remote='true'>
    # <input name='_method' type='hidden' value='patch' />
    # </form>

#### HTML属性を指定
    <%= form_for(@post, data: { behavior: "autosave" }, html: { name: "go" }) do |f| %>
    <% end %>
    # <form action='http://www.example.com' method='post' data-behavior='autosave' name='go'>
    # <input name='_method' type='hidden' value='patch' />
    # </form>

#### 外部リソースへのForm
    <%= form_for @invoice, url: external_url, authenticity_token: 'external_token' do |f| %>
    <% end %>

#### 認証トークンを使わない外部リソースへのForm
    <%= form_for @invoice, url: external_url, authenticity_token: false do |f| %>
    <% end %>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L430)