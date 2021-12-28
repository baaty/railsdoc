---
layout: page
---

### 説明

サイトの名前などのアプリケーションで共通の名前を変数として設定

### 使い方

    config/application.rb
    module モジュール名
      class Application < Rails::Application
        config.変数名 = 値

### 例

#### サイトの名前を変数に設定

##### 設定

    module Mysite
      class Application < Rails::Application
        config.title = "サイトの名前"

##### 参照

    Mysite::Application.config.title
