---
layout: page
---
### 説明
コントローラやアクションなどからURLを生成

### 使い方
    url_for(オプション)

### オプション

オプション           | 説明                         | デフォルト値
----------------|-----------------------------|-------
:controller     | コントローラ名                     |
:action         | アクション名                      |
:anchor         | アンカー(URLの#以降)を指定         |
:only_path      | trueなら、URL全体ではなくパス部分を返す | true
:trailing_slash | 末尾にスラッシュを付与              |
:host           | URLのホストを指定                 |
:protocol       | URLのプロトコルを指定               |
:user           | HTTP認証                     |
:password       | HTTP認証                     |

### 例
#### 基本的な使い方
    url_for controller: 'pages', action: 'show'
    # '/pages/show'

#### コントローラを省略した場合は、現在のコントローラを利用
    url_for controller: 'pages', action: 'show'
    # '/pages/show'

#### 絶対URL
    url_for controller: 'pages', action: 'show', only_path: false
    # 'http://localhost/pages/show'

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/routing_url_for.rb#L79)