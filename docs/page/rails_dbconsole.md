---
layout: page
---

### 説明

コンソールを起動

### 使い方

    $ rails dbconsole [オプション]

#### 短縮形

    $ rails db [オプション]

### オプション

| オプション                    | 説明                                                              |
| ----------------------------- | ----------------------------------------------------------------- |
| -e, --environment=ENVIRONMENT | 環境                                                              |
| -p, --include-password        | database.ymlからパスワードを自動的に付与                          |
| --mode=MODE                   | sqlite3を自動的に指定されたモード(html, list, line, column)に設定 |
| --header                      | ヘッダー                                                          |
| --db, --database=DATABASE     | 使用するデータベースを指定                                        |
| -h, --help                    | ヘルプ                                                            |

### 環境

| 環境        | 説明       |
| ----------- | ---------- |
| development | 開発環境   |
| text        | テスト環境 |
| production  | 本番環境   |

### 例

    $ rails dbconsole
