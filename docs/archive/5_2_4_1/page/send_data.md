---
layout: archive_page
---
### 説明
バイナリデータを出力

### 使い方
    send_data(送るデータ [, オプション])

### オプション

オプション        | 説明                                        | デフォルト値
-------------|---------------------------------------------|-------------------------
:filename    | 保存するときに使用するファイル名                       | ファイル名
:type        | コンテントタイプ                                    | application/octet-stream
:disposition | ファイルをインラインで表示するか、ダウンロードして保存するかブラウザに通知 | attachment
:status      | ステータスコード                                    | 200(:ok)

### 例
#### 基本的な使い方
    send_data buffer

#### 動的に生成
    send_data generate_tgz('dir'), filename: 'dir.tgz'

#### JPEGを表示
    send_file '/path/to.jpeg', type: 'image/jpeg', disposition: 'inline'

#### 404を表示
    send_file '/path/to/404.html', type: 'text/html; charset=utf-8', status: 404

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionpack/lib/action_controller/metal/data_streaming.rb#L108)