---
layout: page
---
### 説明
アプリケーションに最低限必要なフォルダやファイルを自動的に作成

### 使い方
    $ rails new アプリケーション名 [オプション]

### オプション

| オプション | 説明 | デフォルト |
|-|-|-|
| -r, -ruby=PATH | rubyバイナリのパス |  |
| -m, -template=TAMPLATE | テンプレートのパス |  |
| --skip-gemfile | Grmfileを作成しない |  |
| ｰB, --skip-bundle | bundle installを行わない |  |
| -G, --skip-git | .gitignoreを組み込まない |  |
| --skip-keeps | .keepを組み込まない |  |
| -O, --skip-active-recode | active recordを組み込まない |  |
| -S, --skip-sprockets | sprocketsを組み込まない |  |
| --skip-spring | springアプリケーションをインストールしない |  |
| -d, --database=DATABASE | データベースの種類 | sqlite3 |
| -j, --javascript=JAVASCRIPT | 組み込むJavaScriptライブラリーを指定。 | jquery |
| -J, --skip-javascript | javascriptを組み込まない |  |
| --dev | github リポジトリ上の自分のコードから作成 |  |
| --edge | github リポジトリ上の最新のコードから作成 |  |
| -T, --skip-test-unit | test::unitを組み込まない |  |
| --rc=RC |  |  |
| --no-rc |  |  |
| -f, --force | ファイルが存在する場合に上書きする |  |
| -p, --pretend | ドライラン |  |
| -q, --quiet | 進捗情報を表示しない |  |
| -s, --skip | 既に存在するファイルについてはスキップ |  |
| -h, --help | ヘルプ |  |
| -v, --version | バージョンを表示 |  |

### 例
#### アプリケーションを作成
    $ rails new weblog

#### mysqlを使うアプリケーションを作成
    $ rails new weblog -d mysql

#### 古いバージョンのRailsでアプリケーションを作成
    $ rails _3.2.13_ new weblog