---
layout: page
---
### 説明
文字列をエスケープしない。Rails3では、デフォルトで「<%= %>」で出力される値はエスケープ

### 使い方
    raw(文字列)

### エスケープする文字列

変換前 | 変換後    | 説明
--- | ------ | -------------
<   | &lt;   | 右大不等号
>   | &gt;   | 左大不等号
&   | &amp;  | アンドマーク、アンパサンド
"   | &quot; | ダブルクォート

### 例
#### エスケープしないで出力
    <%= raw("<h1>Railsドキュメント</h1>") %>
     # <h1>Railsドキュメント</h1>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/71c7fd101324046995d8f7e51e78475c0e37ec1a/actionview/lib/action_view/helpers/output_safety_helper.rb#L16)