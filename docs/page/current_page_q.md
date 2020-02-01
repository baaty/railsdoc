---
layout: page
---
### 説明
指定したURLが、現在表示されているか？

### 使い方
    current_page?(オプション [, check_parameters: false])

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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/url_helper.rb#L543)