---
layout: page
---
### 説明
assetファイルへのパスを取得

### 使い方
    asset ファイルへのパス [, オプション]

### オプション

オプション | 説明
----- | --------
:type | ファイルのタイプ

### 例
    asset_path "application.js"
    # /application.js

    asset_path "application", type: :javascript
    # /javascripts/application.js

    asset_path "application", type: :stylesheet
    # /stylesheets/application.css

    asset_path "http://www.example.com/js/xmlhr.js"
    # http://www.example.com/js/xmlhr.js

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/457c876b15640d79f4398c3facb8652210d7c2e0/actionview/lib/action_view/helpers/asset_url_helper.rb#L123)