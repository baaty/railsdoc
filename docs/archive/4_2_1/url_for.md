---
layout: page
---
### 説明
アプリケーションを参照するURLを生成

### 使い方
    url_for(オプション)

### オプション

オプション           | 説明                                                                                                                           | デフォルト
--------------- | ---------------------------------------------------------------------------------------------------------------------------- | -----
:anchor         | アンカー(URLの#以降)を指定                                                                                                             |
:only_path      | trueなら、URL全体ではなくパス部分を返す                                                                                                      | false
:trailing_slash | If true, adds a trailing slash, as in “/archive/2005/“. Note that this is currently not recommended since it breaks caching. |
:host           | URLのホストを指定                                                                                                                   |
:protocol       | URLのプロトコルを指定                                                                                                                 |
:user           | インライン認証を指定                                                                                                                   |
:password       | インライン認証を指定                                                                                                                   |

### 例
#### 基本的な使い方
    <%= url_for :controller => 'pages', :action => 'show' %>
    # => '/pages/show'

#### コントローラを省略した場合は、現在のコントローラを利用
    <%= url_for :controller => 'pages', :action => 'show' %>
    # => '/pages/show'

#### 絶対URL
    <%= url_for :controller => 'pages', :action => 'show', :only_path => false %>
    # => 'http://localhost/pages/show'

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/9685080a7677abfa5d288a81c3e078368c6bb67c/actionpack/lib/action_dispatch/routing/url_for.rb#L150)