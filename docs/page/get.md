---
layout: page
---

### 説明

GETリクエスト

### 使い方

    get(URLパターン, 引数..)

### オプション

| オプション           | 説明                                       |
| -------------------- | ------------------------------------------ |
| :controller, :action | コントローラとアクションを必ずセットで指定 |
| :to                  | :controller, :actionの短縮形。#で区切る    |
| :via                 | HTTPメソッドを指定                         |
| :as                  | ルート名に使用する別名                     |

### 例

#### GETリクエスト

    get 'bacon', to: 'food#bacon'

#### コントローラとアクションを指定

    get '/texts', controller: 'texts', action: 'index'

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/routing/mapper.rb#L687)
