---
layout: page
---
### 説明
外部のJacaScriptファイルをインクルード

### 使い方
    javascript_include_tag JavaScriptファイルへのパス [, オプション]

### JavaScriptファイルへのパスの予約語

予約語      | 説明
-------- | ------------------------------------------------
:all     | app/assets/javascripts/フォルダ配下のすべての.jsファイルをインクルード
:default | 特定の.jsファイルをインクルード

### オプション

オプション      | 説明
---------- | -------------
:cache     | キャッシュを有効にするか
:recursive | 再帰的にインクルードするか

### 例
#### 外部のJacaScriptファイルをインクルードタグの生成
    <%= javascript_include_tag "example" %>
    # <script src="/javascripts/example.js" type="text/javascript"></script>

#### 外部のJacaScriptファイルをインクルードタグの生成
    <%= javascript_include_tag "example.js" %>
    # <script src="/javascripts/example.js" type="text/javascript"></script>

#### JacaScriptファイルを複数指定
    <%= javascript_include_tag "example1", "example2" %>
    # <script src="/javascripts/example1.js" type="text/javascript"></script>
    # <script src="/javascripts/example2.js" type="text/javascript"></script>

#### 外部サイトのJacaScriptファイルを指定
    <%= javascript_include_tag "http://www.example.com/example" %>
    # <script src="http://www.example.com/example" type="text/javascript"></script>

#### Railsのデフォルトで使用するJacaScriptを指定
##### jQuery(Rails3.1以上でデフォルトの設定)
    <%= javascript_include_tag :defaults
    # <script src="/javascripts/jquery.js?xxx" type="text/javascript"></script>
    # <script src="/javascripts/rails.js?xxx" type="text/javascript"></script>
    # <script src="/javascripts/application.js?xxx" type="text/javascript"></script>

##### jQueryを使わない(Rails3.1以下でデフォルトの設定)
    <%= javascript_include_tag :defaults
    # <script src="/javascripts/prototype.js?xxx" type="text/javascript"></script>
    # <script src="/javascripts/effects.js?xxx" type="text/javascript"></script>
    # <script src="/javascripts/dragdrop.js?xxx" type="text/javascript"></script>
    # <script src="/javascripts/controls.js?xxx" type="text/javascript"></script>
    # <script src="/javascripts/rails.js?xxx" type="text/javascript"></script>
    # <script src="/javascripts/application.js?xxx" type="text/javascript"></script>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/71c7fd101324046995d8f7e51e78475c0e37ec1a/actionview/lib/action_view/helpers/asset_tag_helper.rb#L56)