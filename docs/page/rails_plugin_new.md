---
layout: page
---

### 説明

プラグインをインストール

### 使い方

    $ rails plugin new パス [オプション]

### オプション

| オプション               | 説明                                                                             | デフォルト値 |
| ------------------------ | -------------------------------------------------------------------------------- | ------------ |
| --skip-namespace         | namespaceの生成をスキップ                                                        |              |
| --skip-collision-check   | コリジョンチェックをスキップ                                                     |              |
| -r, --ruby=PATH          | Rubyのインストールパス                                                           |              |
| -m, --template=TEMPLATE  | プラグインのテンプレートへのパス                                                 |              |
| -d, --database=DATABASE  | データベースの種類                                                               | sqlite3      |
| -G, --skip-git           | .gitignoreファイルの生成をスキップ                                               |              |
| --skip-keeps             | .keepファイルの生成をスキップ                                                    |              |
| -M, --skip-action-mailer | Action Mailerファイルの生成をスキップ                                            |              |
| --skip-action-mailbox    | Action MailboxのGemをスキップ                                                    |              |
| --skip-action-text       | Action TextのGemをスキップ                                                       |              |
| -O, --skip-active-record | Active Recordファイルの生成をスキップ                                            |              |
| --skip-active-job        | Active Jobをスキップ                                                             |              |
| --skip-active-storage    | Active Storageファイルの生成をスキップ                                           |              |
| -C, --skip-action-cable  | Action Cableファイルの生成をスキップ                                             |              |
| -S, --skip-sprockets     | Sprocketsファイルの生成をスキップ                                                |              |
| -J, --skip-javascript    | JavaScriptファイルの生成をスキップ                                               | true         |
| --skip-hotwire           | Hotwireの統合をスキップ                                                          |              |
| --skip-jbuilder          | jbuilderのGemをスキップ                                                          |              |
| -T, --skip-test          | testファイルの生成をスキップ                                                     |              |
| --skip-system-test       | システムテストファイルの生成をスキップ                                           |              |
| --skip-bootsnap          | bootsnapのGem をスキップ                                                         |              |
| --dev                    | githubリポジトリ上の自分のコードから作成                                         |              |
| --edge                   | githubリポジトリ上の最新のコードから生成                                         |              |
| --master, --main         | RailsのメインブランチのGemfileでアプリケーションをセットアップ |              |
| --rc=RC                  | railsコマンドの追加の構成オプションを含むファイルへのパス                        |              |
| --no-rc                  | .railsrcファイルからの追加のロードをスキップ                                     |              |
| --dummy-path=DUMMY_PATH  | 与えられたパスにダミーのアプリケーションを作成                                   | test/dummy   |
| --full                   | テスト用のRailsアプリケーションがバンドルされたRailsエンジンを生成               |              |
| --mountable              | マウント可能な孤立したエンジンを生成                                             |              |
| --skip-gemspec           | gemspecファイルの生成をスキップ                                                  |              |
| --skip-gemfile-entry     | プラグインを作成する場合にGemfileへのエントリ追加をスキップ                      |              |
| --api                    | APIのみのアプリケーションを生成                                                  |              |
| -f, --force              | ファイルが存在する場合に上書き                                                   |              |
| -p, --pretend            | ドライラン                                                                       |              |
| -q, --quiet              | 進捗情報を非表示                                                                 |              |
| -s, --skip               | 既に存在するファイルはスキップ                                           |              |
| -h, --help               | ヘルプ                                                                           |              |
| -v, --version            | バージョンを表示                                                                 |              |

### 例

    $ rails plugin new ~/Code/Ruby/blog
