---
layout: page
---

### 説明

直前のページにリダイレクト

### 使い方

    redirect_back(fallback_location: HTTP_REFERERが設定されていない場合のリダイレクト先, allow_other_host: 許可されたHost=_allow_other_host, 引数..)

### オプション

| オプション        | 説明                                     | デフォルト値 |
| ----------------- | ---------------------------------------- | ------------ |
| :allow_other_host | 異なるホストへのリダイレクトを許可するか | true         |

### 例

#### 直前のページにリダイレクト

    redirect_back fallback_location: { action: "show", id: 5 }

#### インスタンス変数

    redirect_back fallback_location: @post

#### URL

    redirect_back fallback_location: "http://www.rubyonrails.org"

#### 異なるホストへのリダイレクト

    redirect_back fallback_location: '/', allow_other_host: false

### 補足

- Rails5.1以前は「redirect_to :back」

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/redirecting.rb#L95)
