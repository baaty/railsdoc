---
layout: archive_page
---
### 説明
コントローラとビューの生成

### 使い方
    $ rails generate controller 名前 [アクション名...]

### オプション

| オプション                      | 説明                     | 初期値    |
|----------------------------|--------------------------|-----------|
| --skip-namespace           | 名前空間をスキップする          |           |
| --skip-route               | config/routes.rbに追加しない |           |
| -e, --template-engine=NAME | 使用するテンプレートエンジンを指定    | erb       |
| -t, --test-framework=NAME  | 使用するテストフレームワークを指定    | test_unit |
| --helper                   | ヘルパーを生成するか             | true      |
| --assets                   | アセットを生成するか             | true      |
| -f, --force                | ファイルが存在する場合に上書きする  |           |
| -p, --pretend              | ドライラン                    |           |
| -q, --quiet                | 進捗状況を表示しない         |           |
| -s, --skip                 | 既に存在するファイルについてはスキップ   |           |
| -h, --help                 | ヘルプを表示                 |           |

### 例
#### 基本形(オプションなし)
    $ rails generate controller Page
          create  app/controllers/page_controller.rb
          invoke  erb
          create    app/views/page
          invoke  test_unit
          create    test/functional/page_controller_test.rb
          invoke  helper
          create    app/helpers/page_helper.rb
          invoke    test_unit
          create      test/unit/helpers/page_helper_test.rb
          invoke  assets
          invoke    coffee
          create      app/assets/javascripts/page.js.coffee
          invoke    scss
          create      app/assets/stylesheets/page.css.scss

#### アクションとビューも生成
    $ rails generate controller page title
          create  app/controllers/page_controller.rb
           route  get "page/title"
          invoke  erb
          create    app/views/page
          create    app/views/page/title.html.erb
          invoke  test_unit
          create    test/functional/page_controller_test.rb
          invoke  helper
          create    app/helpers/page_helper.rb
          invoke    test_unit
          create      test/unit/helpers/page_helper_test.rb
          invoke  assets
          invoke    coffee
          create      app/assets/javascripts/page.js.coffee
          invoke    scss
          create      app/assets/stylesheets/page.css.scss

#### 階層化されたコントローラを生成
    $ rails generate controller 'admin/page'
          create  app/controllers/admin/page_controller.rb
          invoke  erb
          create    app/views/admin/page
          invoke  test_unit
          create    test/functional/admin/page_controller_test.rb
          invoke  helper
          create    app/helpers/admin/page_helper.rb
          invoke    test_unit
          create      test/unit/helpers/admin/page_helper_test.rb
          invoke  assets
          invoke    coffee
          create      app/assets/javascripts/admin/page.js.coffee
          invoke    scss
          create      app/assets/stylesheets/admin/page.css.scss