---
layout: page
---

### 特徴

- 生成される場所「app/views/layouts」
- JavaScriptやCSSなどもここに記述

### 例

    <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
           "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
    <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
    <head>
      <meta http-equiv="content-type" content="text/html;charset=UTF-8" />
      <title>Title: <%= controller.action_name %></title>
      <%= stylesheet_link_tag 'scaffold' %>
    </head>
    <body>

    <p style="color: green"><%= flash[:notice] %></p>

    <%= yield  %>

    </body>
    </html>

### レイアウトに動的コンテンツを出力

    yield :header

### サブテンプレート

テンプレート内に別のテンプレートを埋め込む

    render file: "shared/bannaer"

#### サブテンプレートに変数を渡す

    render file: "shared/bannaer", locals: { :login_time = sessin[:login_time] || Time.now }

### 部分テンプレート

ビューから部分テンプレートを呼び出す

    render partial: "entry "

#### 部分テンプレートを繰り返し描写

    render partial: "entry", collection: @entries

### スタイルシート

- ファイルの場所「public/stylesheets」

#### スタイルシートのタグ生成

    stylesheet_link_tag "rails", "entries"

#### すべてのスタイルシートを呼び出す

    stylesheet_link_tag :all

#### 複数のスタイルシートを1つにまとめる

    stylesheet_link_tag :all, cache: true

### 使い方

    _テンプレート名.rhtml

### 特徴

- ファイルの場所は、「app/views/コントローラ名/」
- 部分テンプレートを呼び出すには、renderメソッドを使う

  - renderメソッドについて
