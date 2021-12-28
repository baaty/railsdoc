---
layout: page
---

### 説明

文字列をエスケープしない

### 使い方

    raw(文字列)

### エスケープする文字列

| 変換前 | 変換後 | 説明                       |
| ------ | ------ | -------------------------- |
| <   | <   | 右大不等号                 |
| >      | >      | 左大不等号                 |
| &      | &      | アンドマーク、アンパサンド |
| "      | "      | ダブルクォート             |

### 例

#### エスケープしないで出力

    raw "<h1>Railsドキュメント</h1>"
    #=> <h1>Railsドキュメント</h1>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/output_safety_helper.rb#L18)
