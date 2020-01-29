---
layout: page
---
### 説明
未実行のマイグレーションファイルを実行

### 使い方
    $ rake db:migrate [VERSION=バージョン番号] [オプション]

### 実行の流れ
1.  rake db:migrateを実行
2.  schema_migrationsテーブルを調べ、存在しなければ作成
3.  db/migrateディレクトリ内のすべてのマイグレーションファイルを調べる
4.  データベースの現在のバージョンと異なるバージョンがあった場合、データベースに適応
5.  schema_migrationsテーブルの更新

### 詳細

コマンド                                        | 説明
--------------------------------------------|---------------------------------------
rake db:abort_if_pending_migrations         | 実行されていないmigrationを表示
rake db:migrate [VERSION=バージョン番号] [オプション] | db/migrate内のスクリプトファイルからdatabaseにテーブル作成
rake db:migrate:down                        | 指定したmigrationファイルのself.downメソッドを実行
rake db:migrate:redo [STEP=ステップ数]          | 指定したmigrationファイルのself.downメソッドを実行
rake db:migrate:reset                       | databaseを一度削除してもう一度作成し、db:migrate実行
rake db:mgrate:up                           | 指定したmigrationファイルのself.upメソッドを実行

### オプション

オプション     | 説明                                     | デフォルト値
----------|----------------------------------------|------------
RAILS_ENV | testやproduction環境の設定を使用する場合に使用 | development
VERBOSE   | 途中結果を表示するか                         | false

### 例
#### 基本形(オプションなし)
    $ rake db:migrate

#### プロダクション環境のマイグレーション
    $ rake db:migrate RAILS_ENV=production

#### テスト環境のマイグレーション
    $ rake db:migrate RAILS_ENV=test

#### 特定のバージョンのスキーマに変更
    $ rake db:migrate VERSION=201010190000

#### テーブルの初期化
    $ rake db:migrate:reset

#### 一つ前のバージョンに戻す
    $ rake db:migrate:redo STEP=1

#### 指定したマイグレーションのみ実行
    $ rake db:migrate:up VERSION=201010190000

#### スキーマのバージョンを調べる
    $ rake db:version