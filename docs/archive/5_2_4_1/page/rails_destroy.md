---
layout: archive_page
---
### 説明
rails generateで自動生成したファイルを削除

### 使い方
    $ rails destroy ファイルの種類 [削除するファイル名 オプション]

#### 短縮形
     $ rails d ファイルの種類 [削除するファイル名 オプション]

### ファイルの種類
* controller
* generator
* helper
* integration_test
* mailer
* migration
* model
* observer
* performance_test
* plugin
* resource
* scaffold
* scaffold_controller
* session_migration
* stylesheets

### オプション

| オプション         | 説明                  |
| ------------- | ------------------- |
| -h, --help    | ヘルプを表示              |
| -p, --pretend | ドライラン               |
| -f, --force   | ファイルが存在する場合に上書きする   |
| -s, --skip    | 既に存在するファイルについてはスキップ |
| -q, --quiet   | 進捗状況を表示しない          |


### 例
#### helloのコントローラを削除
    $ rails destroy controller hello

#### マイグレーションファイルの削除
    $ rails destroy migration AddSslFlag
       notempty  db/migrate
       notempty  db
             rm  db/migrate/20101030171223_add_ssl_flag.rb

#### プラグインをインストール
    $ rails plugin remove continuous_builder