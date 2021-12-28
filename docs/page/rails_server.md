---
layout: page
---

### 説明

Railsに標準で付随しているPumaをサーバとして起動

### 使い方

    $ rails server -u [Rackサーバーを指定(thin/puma/webrick)] [オプション]

#### 短縮形

    $ rails s [オプション]

### オプション

| オプション             | 説明                                                    | 初期値              |
| ---------------------- | ------------------------------------------------------- | ------------------- |
| -e, --environment=name | 環境(test/development/production)を指定してサーバを起動 | development         |
| -p, --port=port        | サーバを起動するときのポート番号を指定                  | 3000                |
| -b, --binding=ip       | バインドするIPアドレスを指定                            | 0.0.0.0             |
| -c, --config=file      | rackupファイルを指定                                    | config.ru           |
| -d, --daemon           | デーモンとしてサーバを起動                              |                     |
| -u, --using=name       | Rackサーバーを指定                                      |                     |
| -P, --pid=pid          | PIDファイルを指定                                       | tmp/pids/server.pid |
| -C, --dev-caching      | development環境でキャッシュするか                       |                     |
| --early-hints          | HTTP/2のアーリーヒンティングを有効                      |                     |
| --log-to-stdout        | 標準出力にログを出力するか                              |                     |
| -h, --help             | ヘルプを表示                                            |                     |

### 例

#### 開発用WEBサーバを起動

    $ rails server

#### ポート番号を変更

    $ rails server --p=3001

#### デーモンとして起動

    $ rails server --d

#### 本番として起動

    $ rails server -e production

#### 短縮形

    $ rails s
