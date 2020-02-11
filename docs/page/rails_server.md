---
layout: page
---
### 説明
Railsに標準で付随しているPumaをサーバとして起動

### 使い方
    $ rails server [オプション]

#### 短縮形
    $ rails s [オプション]

### オプション

オプション               | 説明                                                | 初期値
---------------------- | --------------------------------------------------- | -------------------
-p, --port=port        | サーバを起動するときのポート番号を指定                    | 3000
-b, --binding=ip       | バインドするIPアドレスを指定                            | 0.0.0.0
-c, --config=file      | rackupファイルを指定                                  |
-d, --daemon           | デーモンとしてサーバを起動                              |
-u, --debugger         | デバックモード                                        |
-e, --environment=name | 環境(test/development/production)を指定してサーバを起動 | development
-P, --pid=pid          | PIDファイルを指定                                     | tmp/pids/server.pid
-h, --help             | ヘルプを表示                                          |

### 例
#### 開発用WEBサーバを起動
    $ rails server
    => Booting Puma
    => Rails 6.0.2.1 application starting in development on http://0.0.0.0:3000
    => Call with -d to detach
    => Ctrl-C to shutdown server

#### ポート番号を変更
    $ rails server --p=3001

#### デーモンとして起動
    $ rails server --d

#### 本番として起動
    $ rails server -e production

#### 短縮形
    $ rails s