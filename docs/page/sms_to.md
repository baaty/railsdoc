---
layout: page
---

### 説明

SMS用のタグを生成

### 使い方

    sms_to(電話番号, リンクテキスト=nil, オプション={}, ブロック引数)

### オプション

| オプション    | 説明                         |
| ------------- | ---------------------------- |
| :country_code | 電話番号の前に国番号を付ける |
| :body         | メッセージの本文             |

### 例

#### SMS用のタグを生成

    sms_to "5155555785"
    #=> <a href="sms:5155555785;">5155555785</a>

#### リンクテキストを指定

    sms_to "5155555785", "Text me"
    #=> <a href="sms:5155555785;">Text me</a>

#### 国番号を付与

    sms_to "5155555785", country_code: "01"
    #=> <a href="sms:+015155555785;">5155555785</a>

#### メッセージの本文

    sms_to "5155555785", body: "I have a question about your product."
    #=> <a href="sms:5155555785;?body=I%20have%20a%20question%20about%20your%20product">5155555785</a>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/url_helper.rb#L665)
