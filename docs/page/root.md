---
layout: page
---
### 説明
ルート(/)のURLを指定

### 使い方
    root(パス, [オプション])

### パス

| オプション                | 説明                                             |
|----------------------|------------------------------------------------|
| :controller, :action | コントローラとアクションを指定。必ずセットで指定                    |
| :to                  | :controller, :actionの短縮形。#でコントローラとアクションを区切る |

### オプション

| オプション        | 説明            |
|--------------|-----------------|
| :param       | パラメータを指定      |
| :path        | パスを指定         |
| :module      | コントローラの名前空間 |
| :as          | ルート名に使用する別名 |
| :via         | HTTPメソッドを指定   |
| :on          | 名前付きルートを指定 |
| :constraints | URLのフォーマットを制限 |
| :defaults    | デフォルト値         |
| :anchor      | アンカーリンク         |
| :format      | フォーマットを指定     |

### 例
#### pagesコントローラとindexアクションをrootに指定
    root controller: 'pages', action: 'index'
    # root  / pages#index

#### コントローラとアクションをtoを使った省略形で記述
    root to: 'pages#index'
    # root  / pages#index

#### toを省略
    root 'pages#index'
    # root  / pages#index

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_dispatch/routing/mapper.rb#L1650)