---
layout: page
---

### 説明

Atomフィードを生成

### 使い方

    atom_feed(オプション, ブロック引数)

### オプション

| オプション   | 説明                          | デフォルト値 |
| ------------ | ----------------------------- | ------------ |
| :language    | 使用する言語                  | en-US        |
| :root_url    | フィードを置き換える文章のURL | /            |
| :url         | フィードのURL                 | 現在のURL    |
| :id          | フィードのid値                |              |
| :schema_date | スキーマ情報                  | 今年         |
| :instruct    | XMLのハッシュ                 |              |

### 例

#### Atomフィードを生成

    atom_feed do |f|
        f.title('新着記事フィード')
        f.updated(@pages.last.created_at)
        @pages.each do |p|
            feed.entry(p, url: p.url, published: p.published, updated: p.updated_at) do |i|
                i.title(p,title)
                i.content("#{@page.published} 公開")
            end
        end
    end

#### 日本語を指定

    atom_feed(language: 'ja-JP') do |f|
        f.title('新着記事フィード')
        f.updated(@pages.last.created_at)
        @pages.each do |p|
            feed.entry(p, url: p.url, published: p.published, updated: p.updated_at) do |i|
                i.title(p,title)
                i.content("#{@page.published} 公開")
            end
        end
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/atom_feed_helper.rb#L98)
