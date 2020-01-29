---
layout: page
---
### 説明
RSSフィードやAtomフィードを自動検出させるlinkタグを生成

### 使い方
    auto_discovery_link_tag(フォードの種類, [フィードへのパス,  オプション])

### オプション

オプション  | 説明       | デフォルト
------ | -------- | -------------------
:rel   | 外部文章との関係 | alternate
:type  | コンテンツタイプ | application/rss+xml
:title | タイトル     | RSS

### 例
#### RSSを自動検出させるタグを生成
    <%= auto_discovery_link_tag %>
    # <link href="http://localhost:3000/" rel="alternate" title="RSS" type="application/rss+xml" />

#### ATOMを自動検出させるタグを生成
    <%= auto_discovery_link_tag(:atom) %>
    # <link href="http://localhost:3000/" rel="alternate" title="ATOM" type="application/rss+xml" />

#### フィードへのパスを指定
    <%= auto_discovery_link_tag(:rss, {:controller => "pages", :action => "feed"}) %>
    # <link href="http://localhost:3000/pages/feed" rel="alternate" title="RSS" type="application/rss+xml" />

#### RSSのタイトルを指定して、RSSを自動検出させるタグを生成
    <%= auto_discovery_link_tag(:rss, "http://www.example.com/feed.rss", :title => "Example RSS") %>
    # <link href="http://www.example.com/feed.rss" rel="alternate" title="Example RSS" type="application/rss+xml" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/71c7fd101324046995d8f7e51e78475c0e37ec1a/actionview/lib/action_view/helpers/asset_tag_helper.rb#L131)