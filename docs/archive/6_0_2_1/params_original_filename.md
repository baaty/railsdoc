---
layout: page
---
### 説明
フォームからアップロードされたファイルを取得

### 使い方
#### ファイル名
    params[:パラメータ名].original_filename

#### コンテンツタイプ
    params[:パラメータ名].content_type

#### サイズ
    params[:パラメータ名].size

#### ファイル本体の読み込み
    params[:パラメータ名].read

### 例
#### アップロードファイルを取得
    params[:file]

#### ファイル名を取得
    params[:file].original_filename

#### 拡張子の取得
    params[:file].content_type

#### ファイルのサイズの取得
    params[:file]

#### ファイル本体の取得
    params[:file].read

#### 基本的な使い方
    def upload
      file = params[:file]
      name = file.original_filename
      if !['.jpg', '.png', '.gif'].include?(File.extname(name).downcase)
        msg = "JPG, PNG, GIFのみアップロードできます。"
      elsif file.size > 10.megabyte
        meg = "10MBまでアップロードできます。"
      else
        File.open("tmp/#{name}", "wb") {|f|f.write(file.read)}
       meg = "アップロードに成功しました。"
      end
      render text: mssg
    end