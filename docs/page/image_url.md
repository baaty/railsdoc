---
layout: page
---

### 説明

画像のURL

### 使い方

    image_url(画像へのパス, オプション={})

### オプション

| オプション | 説明             |
| ---------- | ---------------- |
| :type      | ファイルのタイプ |

### 例

    image_url "edit.png", host: "http://stage.example.com"
    #=> http://stage.example.com/assets/edit.png

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/asset_url_helper.rb#L389)
