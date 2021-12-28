---
layout: page
---

### フォルダとファイルの役割

| ファイル名                                | 説明                                                                    |
| ----------------------------------------- | ----------------------------------------------------------------------- |
| babel.config.js                           | BabelというJavaScript用の設定ファイル                                   |
| config.ru                                 | Rack用のファイル                                                        |
| Gemfile                                   | Gemというパッケージマネージャで依存関係を指定できるファイル             |
| Gemfile.lock                              | Gemfileから実際にインストールされたGemの一覧とバージョン                |
| package.json                              | npmというJavaScriptのパッケージ管理するツール用の設定ファイル           |
| postcss.config.js                         | PostCssというCSS関連のプログラム用の設定ファイル                        |
| Rakefile                                  | RakeというRubyのビルドツール用のファイル                                |
| yam.lock                                  | yamlというパッケージ管理ツール用のファイル                              |
| README.md                                 | 作ったアプリケーションの説明を記述するREADMEファイル                    |
| .git                                      | Git用のディレクトリ                                                     |
| app/                                      | アプリケーション用のディレクトリ                                        |
| app/assets/                               | アプリケーション用のリソースを置くディレクトリ                          |
| app/assets/config/                        | 環境に関するものを管理するファイル用のディレクトリ                      |
| app/assets/images/                        | 画像用のディレクトリ                                                    |
| app/assets/stylesheets/                   | 公開するスタイルシート用のディレクトリ                                  |
| app/channels/                             | Action Cableファイル用のディレクトリ                              |
| app/controllers/                          | コントローラ用のディレクトリ                                            |
| app/controllers/application_controller.rb | アプリケーションで共通のコントローラ                                    |
| app/helpers/                              | ヘルパー用のディレクトリ                                                |
| app/helpers/application_controller.rb     | アプリケーションで共通のヘルパー                                        |
| app/javascript                            | JavaScript関連のスクリプト用のディレクトリ                              |
| app/jobs                                  | Active Job用のディレクトリ                                        |
| app/mailers/                              | Action Mailerファイル用のディレクトリ                              |
| app/mailers/application_mailer.rb         | Action Mailerのコントローラ                                        |
| app/models/                               | モデル用のディレクトリ                                                  |
| app/views/                                | ビュー用のディレクトリ                                                  |
| app/views/layouts/                        | ビューのレイアウト用のRHTMLテンプレート用のディレクトリ                 |
| app/views/layouts/application.html.erb    | アプリケーションで共通のレイアウト                                      |
| app/views/layouts/mailer.html.erb         | Action MailerのHTMLレイアウト                                      |
| app/views/layouts/mailer.text.erb         | Action Mailerのテキストレイアウト                                  |
| bin/                                      | アプリケションを管理する様々なスクリプト用のディレクトリ                |
| config/                                   | アプリケーションの設定ファイル用のディレクトリ                          |
| config/environments/                      | 環境単位の設定ファイル用のディレクトリ                                  |
| config/initializers/                      | 初期化ファイル用のディレクトリ                                          |
| config/locales/                           | 辞書ファイル用のディレクトリ                                            |
| db/                                       | データベース関連のファイル用のディレクトリ                              |
| db/seeds.rb                               | 初期データを生成するファイル                                            |
| lib/                                      | 複数のアプリケーション間で共有するライブラリ用のディレクトリ            |
| lib/assets/                               | 自分で生成したライブラリ用のディレクトリ                                |
| lib/tasks/                                | 自分で生成したRakefile用のディレクトリ                                  |
| log/                                      | ログファイル用のディレクトリ                                            |
| node_modules                              | npmというJavaScriptのパッケージ管理ツールがインストールするディレクトリ |
| public/                                   | Web上に公開するファイル用のディレクトリ                                 |
| storage/                                  | ファイルのアップロードで保存されるディレクトリ                          |
| tmp/                                      | キャッシュなど、一時的なファイル用のディレクトリ                        |
| test/                                     | アプリケーションのテストに使うファイル用のディレクトリ                  |
| temp                                      | 一時ファイル用のディレクトリ                                            |
| vendor/                                   | 外部ライブラリ用のディレクトリ                                          |
| .browserslistrc                           | bowerというパッケージツール用の設定ファイル                             |
| .gitignore                                | Gitに登録しないファイルを指定                                           |
| .ruby-version                             | Rubyのデフォルトバージョン                                              |
