---
layout: page
---
### 説明
assetファイルへのパスを取得

### 使い方
    asset_path(ファイルへのパス [, オプション])

### オプション

オプション          | 説明
---------------|-----------------
:type          | ファイルのタイプ
:skip_pipeline | assetsのpathを付けない
:extname       | 拡張子指定

### 例
#### assetファイルへのパスを取得
    asset_path "application.js"
    # "/assets/application-60aa4fdc5cea14baf5400fba1abf4f2a46a5166bad4772b1effe341570f07de9.js"

#### assetsのpathを付けない
    asset_path "application.js", skip_pipeline: true
    # "application.js"

#### javascriptへのパスを取得
    asset_path "application", type: :javascript
    # /javascripts/application.js

#### stylesheetへのパスを取得
    asset_path "application", type: :stylesheet
    # /stylesheets/application.css

#### 絶対パス指定
    asset_path "/foo.png"
    # "/foo.png"

#### URLを指定してパスを取得
    asset_path "http://www.example.com/js/xmlhr.js"
    # http://www.example.com/js/xmlhr.js

#### 拡張子指定
    asset_path "foo", skip_pipeline: true, extname: ".js"
    # "/foo.js"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/asset_url_helper.rb#L184)