---
layout: page
---

### 説明

入力フィールドのスコープを指定

### 使い方

    fields(スコープ=nil, model: モデル=nil, オプション引数, ブロック引数)

    # f.object
    f.fields(スコープ=nil, model: モデル=nil, オプション引数, ブロック引数)

### オプション

| オプション          | 説明                                        | デフォルト値 |
| ------------------- | ------------------------------------------- | ------------ |
| :as                 | ハッシュのキー名前                          |              |
| :url                | フォームの送信先                            |              |
| :namespace          | 名前空間の設定                              |              |
| :method             | メソッド(get, post, patch, put, deleteなど) |              |
| :authenticity_token | 認証トークン                                |              |
| :remote             | JavaScriptを使うか                          | false        |
| :enforce_utf8       | utf8用の非表示用を出力するか?               | true         |
| :html               | タグの属性                                  |              |
| :format             | フォーマット                                |              |

### 例

    fields :comment do |fields|
        fields.text_field :body
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_helper.rb#L1071)
