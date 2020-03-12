---
layout: archive_page
---
### 説明
決められた記述で書かれたコメントやクラス定義からドキュメントを生成  
生成したドキュメントは、/doc/app/indec/htmlからアクセスする

### 使い方
    $ rake doc:app

### 例
    $ rake doc:app
    rm -r doc/app
    Parsing sources...
    100% [ 3/ 3]  app/helpers/application_helper.rb

    Generating Darkfish format into /xxx/rails/xxx/doc/app...

    Files:      3

    Classes:    1 (1 undocumented)
    Modules:    1 (1 undocumented)
    Constants:  0 (0 undocumented)
    Attributes: 0 (0 undocumented)
    Methods:    0 (0 undocumented)

    Total:      2 (2 undocumented)
      0.00% documented

    Elapsed: 0.3s