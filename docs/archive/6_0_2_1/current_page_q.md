---
layout: page
---
### 説明
指定したURLが、現在表示されているか？

### 使い方
    current_page?(オプション)

### 例
    current_page?(action: 'process')
    # false

    current_page?(action: 'checkout')
    # true

    current_page?(controller: 'library', action: 'checkout')
    # false

    current_page?(controller: 'shop', action: 'checkout')
    # true

    current_page?(controller: 'shop', action: 'checkout', order: 'asc')
    # false

    current_page?(controller: 'shop', action: 'checkout', order: 'desc', page: '1')
    # true

    current_page?(controller: 'shop', action: 'checkout', order: 'desc', page: '2')
    # false

    current_page?('http://www.example.com/shop/checkout')
    # true

    current_page?('http://www.example.com/shop/checkout', check_parameters: true)
    # false

    current_page?('/shop/checkout')
    # true

    current_page?('http://www.example.com/shop/checkout?order=desc&page=1')
    # true

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/url_helper.rb#L543)