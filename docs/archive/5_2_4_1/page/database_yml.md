---
layout: archive_page
---
### 説明
Railsで使うデータベースの設定を記述

### 特徴
* YAML形式で記述
* 開発(development)、テスト(test)、本番(production)の3つの環境

### 接続できるデータベース
* DB2
* Firebird
* Frontbase
* MySQL
* Openbase
* Oracle
* PostgreSQL
* SQLite
* SQL Server
* Sybase

### SQLite3
#### 設定項目

設定項目 | 説明              | デフォルト値
---------|-------------------|---------------
adapter  | 接続するデータベースの種類 | sqlite3
database | データベースファイルまでのパス   | db/環境名.sqlite3
pool     | 接続のブール数        | 5
timeout  | タイムアウト時間        | 5000

#### 例
    development:
      adapter: sqlite3
      database: db/development.sqlite3
      timeout: 5000

    test:
      adapter: sqlite3
      database: db/test.sqlite3
      timeout: 5000

    production:
      adapter: sqlite3
      database: db/production.sqlite3
      timeout: 5000

### MySQL
#### 設定項目

設定項目 | 説明                                          | デフォルト値
---------|-----------------------------------------------|-----------------
adapter  | 接続するデータベースの種類                             | mysql2
database | 接続先のデータベース名                               | db/アプリケーション名_環境名
host     | 接続先のサーバ名またはIPアドレス。socketを指定した場合には無効 | localhost
post     | 接続先のポート番号。socketを指定した場合には無効        | 3306
socket   | Unixソケットのパス                                   | /tmp/mysql.sock
username | データベースに接続するユーザ名                            | root
password | DBに接続するパスワード                                |
encoding | 文字エンコーディングを明示的に指定                      | utf8
pool     | 接続のブール数                                    | 5
timeout  | タイムアウト時間                                    | false