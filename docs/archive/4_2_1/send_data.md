---
layout: page
---
### 説明
動的に生成されたデータのダウンロード

### 使い方
    send_data(送るデータ [, オプション])

### オプション

オプション        | 説明                                    | デフォルト
------------ | ------------------------------------- | ------------------------
:filename   |  データを保存するときに使用するファイル名                  | ファイル名
:type        | コンテントタイプ                              | application/octet-stream
:disposition | ファイルをインラインで表示するか、ダウンロードして保存するかブラウザに通知 | attachment
:status      | ステータスコード                              | 200(:ok)

### 例
    send_data image.data, :type => image.content_type, :disposition => 'inline'

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/e220a34e396f026bbee8c7492aaa0ca515995a05/actionpack/lib/action_controller/metal/data_streaming.rb#L127)