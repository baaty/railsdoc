---
layout: archive_page
---
### 説明
直前のページにリダイレクト

### 使い方
    redirect_back(HTTP_REFERERが設定されていない場合のリダイレクト先 [, オプション])

### オプション

オプション              | 説明                    | デフォルト値
-------------------|-------------------------|-------
:fallback_location |                         |
:allow_other_host  | 異なるホストへのリダイレクトを許可するか | true

### 例
#### 直前のページにリダイレクト
    redirect_back fallback_location: { action: "show", id: 5 }

#### インスタンス変数
    redirect_back fallback_location: @post

#### URL
    redirect_back fallback_location: "http://www.rubyonrails.org"

#### 相対パス
    redirect_back fallback_location: "/images/screenshot.jpg"

#### 異なるホストへのリダイレクト
    redirect_back fallback_location: '/', allow_other_host: false

### 補足
* Rails5.1以前は「redirect_to :back」

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionpack/lib/action_controller/metal/redirecting.rb#L90)