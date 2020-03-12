---
layout: archive_page
---
### 説明
JacaScriptファイルをインクルード

### 使い方
    javascript_include_tag(JavaScriptファイルへのパス [, オプション])

### JavaScriptファイルへのパスの予約語

予約語      | 説明
-------- | ------------------------------------------------
:all     | app/assets/javascripts/フォルダ配下のすべての.jsファイルをインクルード
:default | 特定の.jsファイルをインクルード

### オプション

オプション      | 説明
---------- | -------------
:extname   | 拡張子がない場合に拡張子を追加
:protocol | プロトコルを指定
:host     | 相対パスの場合にホストを追加
:skip_pipeline | アセットパイプラインをスキップ
:nonce | nonce属性

### 例
#### JacaScriptファイルをインクルード
    javascript_include_tag "xmlhr"
    # <script src="/assets/xmlhr.debug-1284139606.js"></script>

#### ホストを指定
    javascript_include_tag "xmlhr", host: "localhost", protocol: "https"
    # <script src="https://localhost/assets/xmlhr.debug-1284139606.js"></script>

#### 拡張子を指定
    javascript_include_tag "template.jst", extname: false
    # <script src="/assets/template.debug-1284139606.jst"></script>

#### .js拡張を指定
    javascript_include_tag "xmlhr.js"
    # <script src="/assets/xmlhr.debug-1284139606.js"></script>

#### 複数指定
    javascript_include_tag "common.javascript", "/elsewhere/cools"
    # <script src="/assets/common.javascript.debug-1284139606.js"></script>
    # <script src="/elsewhere/cools.debug-1284139606.js"></script>

#### URL指定
    javascript_include_tag "http://www.example.com/xmlhr"
    # <script src="http://www.example.com/xmlhr"></script>

#### nonce属性を指定
    javascript_include_tag "http://www.example.com/xmlhr.js", nonce: true
    # <script src="http://www.example.com/xmlhr.js" nonce="..."></script>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/asset_tag_helper.rb#L87)