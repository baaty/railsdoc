---
layout: page
---
### 説明
Atomフィードを生成

### 使い方
    atom_feed([オプション]) do |f|
    end

### オプション

オプション        | 説明               | デフォルト
------------ | ---------------- | -------------------------------------------------------------------------------
:language    | 使用する言語           | en-US
:root_url    | フィードを置き換える文章のURL | /
:url         | フィードのURL         | 現在のURL
:id          | フィードのid値         | tag:#{request.host},#{options[:schema_date]}:#{request.fullpath.split(”.“)}/td>
:schema_date | スキーマ情報           | 今年
:instruct    | XMLのハッシュ         |

### 例
#### Atomフィードを生成
    atom_feed do |f|
        f.title('新着記事フィード')
        f.updated(@pages.last.created_at)
        @pages.each do |p|
            feed.entry(p, :url => p.url, :published => p.published, :updated => p.updated_at) do |i|
                i.title(p,title)
                i.content("#{@page.published} 公開")
            end
        end
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/2ddbe87e7acc324ce7e0a4784c4d10b79cc49a40/actionview/lib/action_view/helpers/atom_feed_helper.rb#L96)