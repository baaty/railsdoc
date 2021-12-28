---
layout: page
---

### 説明

電話番号へのアンカーリンクを生成

### 使い方

    phone_to(電話番号, リンクテキスト=nil, オプション={}, ブロック引数)

### オプション

| オプション    | 説明                         |
| ------------- | ---------------------------- |
| :country_code | 電話番号の前に国番号を付ける |

### 例

#### 電話番号のタグを生成

    phone_to "1234567890"
    #=> <a href="tel:1234567890">1234567890</a>

#### リンクテキストを指定

    phone_to "1234567890", "Phone me"
    #=> <a href="tel:1234567890">Phone me</a>

#### 国番号を付与

    phone_to "1234567890", country_code: "01"
    #=> <a href="tel:+011234567890">1234567890</a>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/url_helper.rb#L716)
