---
layout: page
---

### 説明

ブラウザがプリロードに使用できるリンクタグ

### 使い方

    preload_link_tag(パス, オプション={})

### オプション

| オプション   | 説明                                         |
| ------------ | -------------------------------------------- |
| :type        | MIMEタイプを上書き                           |
| :as          | as属性を上書き                               |
| :crossorigin | クロスオリジン属性を指定                     |
| :nopush      | リソースにサーバープッシュの使用を望まないか |
| :integrity   | 整合性属性を指定                             |

### 例

#### ファイル名を指定

    preload_link_tag("custom_theme.css")
    #=> <link rel="preload" href="/assets/custom_theme.css" as="style" type="text/css" />

#### 相対パスを指定

    preload_link_tag("/videos/video.webm")
    #=> <link rel="preload" href="/videos/video.mp4" as="video" type="video/webm" />

#### パスを指定

    preload_link_tag(post_path(format: :json), as: "fetch")
    #=> <link rel="preload" href="/posts.json" as="fetch" type="application/json" />

#### ファイルパスを指定

    preload_link_tag("//example.com/font.woff2")
    #=> <link rel="preload" href="//example.com/font.woff2" as="font" type="font/woff2" crossorigin="anonymous"/>

#### クロスオリジン属性を指定

    preload_link_tag("//example.com/font.woff2", crossorigin: "use-credentials")
    #=> <link rel="preload" href="//example.com/font.woff2" as="font" type="font/woff2" crossorigin="use-credentials" />

#### リソースにサーバープッシュの使用を望まない

    preload_link_tag("/media/audio.ogg", nopush: true)
    #=> <link rel="preload" href="/media/audio.ogg" as="audio" type="audio/ogg" />

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/asset_tag_helper.rb#L319)
