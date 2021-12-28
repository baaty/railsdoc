---
layout: page
---

### 説明

指定したパスに存在する画像やファイルを読み込みその内容をクライアントに送信

### 使い方

    send_file(ファイルのパス, オプション={})

### オプション

| オプション          | 説明                                                                       | デフォルト値             |
| ------------------- | -------------------------------------------------------------------------- | ------------------------ |
| :filename           | ダウンロードするときに使用するファイル名を指定                             | ファイル名               |
| :type               | コンテントタイプ                                                           | application/octet-stream |
| :disposition        | ファイルをインラインで表示するか、ダウンロードして保存するかブラウザに通知 | attachment               |
| :status             | ステータスコード                                                           | 200(:ok)                 |
| :url_based_filename | Content-Dispositionヘッダ内のファイルのベース名を使わなくする              | false                    |
| :length             | 送信されようとしているコンテンツのサイズ                                   |                          |
| :stream             | falseの場合、ファイル全体が読み込まれてから表示                            |                          |
| :buffer_size        | ストリーミングがtrueの時に、1回に送信されるデータ量                        |                          |
| :x_sendfile         | lighttpdやapacheで利用できるローカルファイル送信用モジュール               |                          |

### 例

#### 指定されたzipファイルをダウンロード

    send_file '/path/to.zip'

#### 指定されたPDFをtest.pdfという名前でダウンロード

    send_file '/path/test_pdf.pdf', filename: 'test.pdf'

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/data_streaming.rb#L69)
