---
layout: page
---
### 説明
指定したURLが、現在表示されていればtrueを返す

### 使い方
    current_page?(オプション)

### 例
#### 表示しているページ(/pages/index)
    current_page?(:action => 'new')
    # false

    current_page?(:controller => 'pages', :action => 'index')
    # true

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/606ce3f907cbccd9159bb558c0b57433b42f3975/actionview/lib/action_view/helpers/url_helper.rb#L525)