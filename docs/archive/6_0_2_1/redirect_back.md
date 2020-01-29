---
layout: page
---
### 説明
直前のページにリダイレクト

### 使い方
    redirect_back(fallback_location: URL [, オプション])

### オプション

オプション             | 説明                    | デフォルト値
------------------|-----------------------|-------
:allow_other_host | 異なるホストへのリダイレクトを許可するか | true

### 例
    redirect_back fallback_location: { action: "show", id: 5 }

    redirect_back fallback_location: @post

    redirect_back fallback_location: "http://www.rubyonrails.org"

    redirect_back fallback_location: "/images/screenshot.jpg"

    redirect_back fallback_location: posts_url

    redirect_back fallback_location: proc { edit_post_url(@post) }

    redirect_back fallback_location: '/', allow_other_host: false

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_controller/metal/redirecting.rb#L90)