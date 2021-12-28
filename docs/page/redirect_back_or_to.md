---
layout: page
---

### 説明

直前のページにリダイレクトしなければ指定したページへリダイレクト

### 使い方

    redirect_back_or_to(fallback_location, allow_other_host: 異なるホストへのリダイレクトを許可するか=_allow_other_host, オプション引数)

### オプション

| オプション | 説明                                 |
| ---------- | ------------------------------------ |
| :alert     | エラーメッセージを表示               |
| :notice    | 通知用のメッセージを表示             |
| :flash     | パラメータを使って、一時的に値を保存 |

### 例

#### actionで指定

    redirect_back_or_to({ action: "show", id: 5 })

#### URLで指定

    redirect_back_or_to "http://www.rubyonrails.org"

#### 相対パスで指定

    redirect_back_or_to "/images/screenshot.jpg"

#### 異なるホストへのリダイレクトを許可しない

    edirect_back_or_to '/', allow_other_host: false

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/redirecting.rb#L121)
