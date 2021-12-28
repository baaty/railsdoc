---
layout: page
---

### 説明

新しいRailsのアプリケーションを作成  
アプリケーションに最低限必要なフォルダやファイルが自動的に生成される

### 使い方

    $ rails new アプリケーション名 [オプション]

### オプション

| オプション                  | 説明                                                                             | デフォルト値 |
| --------------------------- | -------------------------------------------------------------------------------- | ------------ |
| --skip-namespace            | namespaceの生成をスキップ                                                        |              |
| --skip-collision-check      | コリジョンチェックをスキップ                                                     |              |
| -r, -ruby=PATH              | rubyバイナリのパス                                                               |              |
| -m, -template=TAMPLATE      | テンプレートのパス                                                               |              |
| -d, --database=DATABASE     | データベースの種類                                                               | sqlite3      |
| -G, --skip-git              | .gitignoreファイルの生成をスキップ                                               |              |
| --skip-keeps                | .keepファイルの生成をスキップ                                                    |              |
| -M, --skip-action-mailer    | Action Mailerファイルの生成をスキップ                        |              |
| --skip-action-mailbox       | Action MailboxのGemをスキップ                          |              |
| --skip-action-text          | Action TextのGemをスキップ                                   |              |
| -O, --skip-active-recode    | Active Recordファイルの生成をスキップ                        |              |
| --skip-active-job           | Active Jobをスキップ                                           |              |
| --skip-active-storage       | Active Storageファイルの生成をスキップ                     |              |
| -C, --skip-action-cable     | Action Cableファイルの生成をスキップ                         |              |
| -S, --skip-sprockets        | Sprocketsファイルの生成をスキップ                                                |              |
| -J, --skip-javascript       | JavaScriptファイルの生成をスキップ                                               |              |
| --skip-hotwire              | Hotwireの統合をスキップ                                                          |              |
| --skip-jbuilder             | jbuilderのGemをスキップ                                                          |              |
| -T, --skip-test             | testファイルの生成をスキップ                                                     |              |
| --skip-system-test          | システムテストファイルの生成をスキップ                                           |              |
| --skip-bootsnap             | bootsnapのGemをスキップ                                                          |              |
| --dev                       | githubリポジトリ上の自分のコードから作成                                         |              |
| --edge                      | githubリポジトリ上の最新のコードから生成                                         |              |
| --master, --main            | RailsのメインブランチのGemfileでアプリケーションをセットアップ |              |
| --rc=RC                     | railsコマンドの追加の構成オプションを含むファイルへのパス                        |              |
| --no-rc                     | .railsrcファイルからの追加のロードをスキップ                                     |              |
| --api                       | APIのみのアプリケーションを生成                                                  |              |
| --minimal                   | 最小限のRailsアプリケーションを生成                                              |              |
| -j, --javascript=JAVASCRIPT | 組み込むJavaScriptライブラリーを指定                                             | importmap    |
| --css=CSS                   | CSSプロセッサを選択                                                              |              |
| ｰB, --skip-bundle           | bundle installしない                                                             |              |
| -f, --force                 | ファイルが存在する場合に上書き                                                   |              |
| -p, --pretend               | ドライラン                                                                       |              |
| -q, --quiet                 | 進捗情報を非表示                                                                 |              |
| -s, --skip                  | 既に存在するファイルはスキップ                                           |              |
| -h, --help                  | ヘルプ                                                                           |              |
| -v, --version               | バージョンを表示                                                                 |              |

### 例

#### 新しいRailsのアプリケーションを作成

    $ rails new weblog

#### mysqlを使うアプリケーション

    $ rails new weblog -d mysql

#### APIのみのアプリケーション

    $ rails new weblog --api

#### 古いバージョンのRailsでアプリケーション

    $ rails _6.1.4_ new weblog
