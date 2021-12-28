---
layout: page
---

### 説明

指定したURLが現在表示されているかチェック

### 使い方

    current_page?(オプション=nil, check_parameters: チェックパラメータ=false, オプション引数)

### 例

#### 表示されていない場合

    current_page?(action: 'process')
    # false

#### アクションを指定

    current_page?(action: 'checkout')
    # true

#### コントローラとアクションを指定

    current_page?(controller: 'library', action: 'checkout')
    # false

#### パラメータを指定

    current_page?(controller: 'shop', action: 'checkout', order: 'asc')
    # false

#### URLを指定

    current_page?('http://www.example.com/shop/checkout')
    # true

#### パラメータをチェック

    current_page?('http://www.example.com/shop/checkout', check_parameters: true)
    # false

#### クエリを指定

    current_page?('http://www.example.com/shop/checkout?order=desc&page=1')
    # true

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/url_helper.rb#L582)
