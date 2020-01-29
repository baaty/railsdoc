---
layout: page
---
### 説明
アプリケーションの基本的な機能の一覧(index)、詳細(show)、新規作成(new/create)、編集(edit/update)、削除(destroy)を行うために必要なコントローラ、モデル、ビューをまとめて生成

### 使い方
    $ rails generate scaffold 名前 [カラム名:型]

### オプション

オプション                       | 説明
--------------------------- | ----------------------------------------
-r, -ruby=PATH              | rubyバイナリのパス
-b, --builder-BUILDER       | builderのパスを指定
-m, -template=TAMPLATE      | テンプレートのパス
--skip-gemfile              | Grmfileを作成しない
--skip-bundle               | bundle installを行わない
-G, --skip-git              | .gitignore, .gitkeepを組み込まない
-O, --skip-active-recode    | active recordを組み込まない
-S, --skip-sprockets        | sprocketsファイルをスキップ
-d, --database=DATABASE     | データベースの種類
-j, --javascript=JAVASCRIPT | 組み込むJavascriptライブラリーを指定。デフォルトは、jquery
-J, --skip-javascript       | javaScriptを組み込まない
--dev                       | github リポジトリ上の自分のコードから作成
--edge                      | github リポジトリ上の最新のコードから作成
-T, --skip-test-unit        | test::unitを組み込まない
--old-style-hash            | 古いハッシュ形式(:foo => 'bar')を有効にする(Ruby1.9以上)
-f, --force                 | ファイルが存在する場合に上書きする
-p, --pretend               | ドライラン
-q, --quiet                 | 進捗情報を表示しない
-s, --skip                  | 既に存在するファイルについてはスキップ
-h, --help                  | ヘルプ
-v, --version               | バージョンを表示

### カラムの型

データ方      | 説明
--------- | --------
string    | 文字列
text      | 長い文字列
integer   | 整数
float     | 浮動小数
decimal   | 精度の高い小数
datetime  | 日時
timestamp | より細かい日時
time      | 時間
date      | 日付
binary    | バイナリデータ
boolean   | Boolean型

### 生成されるファイル

ファイル                                      | 説明
----------------------------------------- | ----------------------
db/migrate/YYYYMMDDHHMMSS_create_XXXs.rb  | マイグレーションファイル
app/assets/javascripts/XXXs.js.coffee     | モデル固有のCoffeeScript
app/assets/stylesheets/XXXs.css.scss      | モデル固有のSCSSスタイルシート
app/assets/stylesheets/scaffolds.css.scss | Scaffold共通のSCSSスタイルシート
app/controllers/XXXs_controller.rb        | コントローラファイル
app/views/XXXs/index.html.erb             | すべてのリストを表示
app/views/XXXs/edit.html.erb              | 編集ファイル
app/views/XXXs/show.html.erb              | 詳細ページ
app/views/XXXs/new.html.erb               | 新規ページ
app/views/XXXs/_form.html.erb             | フォーム用ページ
app/models/XXX.rb                         | モデルファイル
app/helpers/XXXs_helper.rb                | ヘルパー
test/functional/XXXs_controller_test.rb   | コントローラ用テストファイル
test/unit/XXX_test.rb                     | モデル用テストファイル
test/fixtures/XXXs.yml                    | fixtureファイル
test/unit/helpers/XXXs_helper_test.rb     | テスト用
public/stylesheets/scaffold.css           | デフォルトのスタイルシート

### 例
    $ rails generate scaffold page name:string title:string
          invoke  active_record
          create    db/migrate/YYYYMMDDHHMMSS_create_pages.rb
          create    app/models/page.rb
          invoke    test_unit
          create      test/unit/page_test.rb
          create      test/fixtures/pages.yml
           route  resources :pages
          invoke  scaffold_controller
          create    app/controllers/pages_controller.rb
          invoke    erb
          create      app/views/pages
          create      app/views/pages/index.html.erb
          create      app/views/pages/edit.html.erb
          create      app/views/pages/show.html.erb
          create      app/views/pages/new.html.erb
          create      app/views/pages/_form.html.erb
          invoke    test_unit
          create      test/functional/pages_controller_test.rb
          invoke    helper
          create      app/helpers/pages_helper.rb
          invoke      test_unit
          create        test/unit/helpers/pages_helper_test.rb
          invoke  assets
          invoke    coffee
          create      app/assets/javascripts/pages.js.coffee
          invoke    scss
          create      app/assets/stylesheets/pages.css.scss
          invoke  scss
          create    app/assets/stylesheets/scaffolds.css.scss