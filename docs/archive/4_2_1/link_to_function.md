---
layout: page
---
### 説明
JavaScriptを実行

### 使い方
    link_to_function(名前, メソッド [, オプション])

### 例
    link_to_function "Greeting", "alert('Hello world!')", class: "nav_link"
    # => <a class="nav_link" href="#" onclick="alert('Hello world!'); return false;">Greeting</a>