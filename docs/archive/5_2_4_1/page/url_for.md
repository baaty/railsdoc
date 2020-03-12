---
layout: archive_page
---
### 説明
コントローラやアクションなどからURLを生成

### 使い方
    url_for([オプション])

### オプション

オプション           | 説明                         | デフォルト値
----------------|-----------------------------|-------
:controller     | コントローラ名                     |
:action         | アクション名                      |
:id             | IDを指定                      |
:only_path      | trueなら、URL全体ではなくパス部分を返す | false
:protocol       | URLのプロトコルを指定               | http
:host           | URLのホストを指定                 |
:subdomain      | サブドメインを指定                  |
:tld_length     | TLDレングスを指定                 | 1
:port           | ポート番号を指定                 |
:anchor         | アンカー(URLの#以降)を指定         |
:params         | パラメータを指定                   |
:trailing_slash | 末尾にスラッシュを付与              |
:script_name    | スクリプト名を指定                 |
:locale         | ロケールを指定                    |
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/routing_url_for.rb#L79)