---
layout: page
---
### 説明
プラグインをインストール

### 使い方
    $ rails plugin install [プラグイン名/githubのURL] [オプション]

### オプション

オプション                    | 説明
------------------------ | -------------------------
-x, --externals          | プラグインを取得するsvnを指定
-o, --checkout           | プラグインを取得するsvn checkoutを指定
-e, --export             | プラグインを取得するsvn exportを指定
-q, --quiet              | 進捗状況を表示しない
-r, --revision REVISION |  チェックアウトするリビジョン番号を指定
-f, --force              | ファイルが存在する場合に上書きする
-h, --help               | ヘルプを表示

### 例
#### プラグインをインストール
    $ rails plugin install continuous_builder asset_timestamping