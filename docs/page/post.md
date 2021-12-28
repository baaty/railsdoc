---
layout: page
---

### 説明

POSTリクエスト

### 使い方

    post(URLパターン.., ブロック引数)

### オプション

| オプション           | 説明                                                              |
| -------------------- | ----------------------------------------------------------------- |
| :controller, :action | コントローラとアクションを指定。必ずセットで指定                  |
| :to                  | :controller, :actionの短縮形。#でコントローラとアクションを区切る |
| :via                 | HTTPメソッドを指定                                                |
| :as                  | ルート名に使用する別名                                            |

### 例

#### POSTリクエスト

    post 'bacon', to: 'food#bacon'

#### toオプション

    post '/projects/add_users', to: 'projects#add_users'

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/routing/mapper.rb#L695)
