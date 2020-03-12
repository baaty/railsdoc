---
layout: archive_page
---
### 説明
* 使用するレイアウトを明示的に指定
* 指定しない場合は、app/views/layouts/コントローラ名.html.erbを使用
* app/views/layouts/コントローラ名.html.erbが無い場合は、app/views/layouts/application.html.erbを使用

### 使い方
    layout レイアウト名

### 例
#### 基本となる使い方
    layout bank_standard

#### 動的にレイアウトを変える
    layout :writers_and_readers
    private
    def writers_and_readers
      logged_in? ? "writer_layout" : "reader_layout"
    end

#### 特定のアクションのみにレイアウトを指定
    layout weblog_standard, only: :rss

#### 特定のアクション以外にレイアウトを指定
    layout weblog_standard, except: :rss