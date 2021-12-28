---
layout: page
---

### 説明

ルートのデフォルトパラメーターを設定

### 使い方

    defaults(デフォルトパラメータ={})

### 例

    defaults id: 'home' do
        match 'scoped_pages/(:id)', to: 'pages#show'
    end

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/routing/mapper.rb#L1008)
