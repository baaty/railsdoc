---
layout: archive_page
---
### 説明
ブロック内の実行時間を測定し結果をログに記録

### 使い方
    benchmark([メッセージ, オプション])

### オプション

オプション    | 説明
---------|----------------
:level   | ログレベル
:silence | ブロック内でのログ出力をしない

### 例
#### ブロック内の実行時間を測定し結果をログに記録
    <% benchmark 'Process data files' do %>
      <%= expensive_files_operation %>
    <% end %>

#### ログレベルを指定
    <% benchmark 'Low-level files', level: :debug do %>
      <%= lowlevel_files_operation %>
    <% end %>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activesupport/lib/active_support/benchmarkable.rb#L37)