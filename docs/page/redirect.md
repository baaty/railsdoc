---
layout: page
---

### 説明

任意のパスを別のパスにリダイレクト

### 使い方

    redirect(パス.., ブロック引数)

### 例

#### リダイレクト

    get "/stories" => redirect("/posts")

#### 引数で補完

    get 'docs/:article', to: redirect('/wiki/%{article}')

#### ブロック

    get 'jokes/:number', to: redirect { |params, request|
        path = (params[:number].to_i.even? ? "wheres-the-beef" : "i-love-lamp")
        "http://#{request.host_with_port}/#{path}"
    }

#### 変更が必要なURL

    get 'stores/:name', to: redirect(subdomain: 'stores', path: '/%{name}')

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/routing/redirection.rb#L185)
