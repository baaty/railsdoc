---
layout: page
---

### 説明

rails generateで自動生成したファイルを削除

### 使い方

    $ rails destroy ファイルの種類 [削除するファイル名] [オプション]

#### 短縮形

     $ rails d ファイルの種類 [削除するファイル名[ [オプション]

### ファイルの種類

- application_record
- benchmark
- channel
- controller
- generator
- helper
- integration_test
- jbuilder
- job
- mailbox
- mailer
- migration
- model
- resource
- scaffold
- scaffold_controller
- system_test
- task

### オプション

| オプション    | 説明                                   |
| ------------- | -------------------------------------- |
| -h, --help    | ヘルプを表示                           |
| -p, --pretend | ドライラン                             |
| -f, --force   | ファイルが存在する場合に上書き         |
| -s, --skip    | 既に存在するファイルはスキップ |
| -q, --quiet   | 進捗状況を表示しない                   |

### 例

#### helloのコントローラを削除

    $ rails destroy controller hello

#### マイグレーションファイルの削除

    $ rails destroy migration AddSslFlag
