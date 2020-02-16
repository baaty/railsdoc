---
layout: page
---
### 説明
モデルからデータを受け取り、ビューにレンダリングを行わせる仕組み

### 特徴
* コントローラには複数のアクションが含まれている
* コントローラの名前の付け方には決まりがある

### 規約
* 英大文字から始まる
* 英数字のみ
* 単語の区切りでは、先頭文字を大文字
  * EntriesController
  * UserCommentsController
* ファイルはapp/controllerディレクトリに格納
* ファイル名は、コントローラ名の単語区切りを「_」にし、すべて小文字にしたもの
  * app/controllers/entries_controller.rb
  * app/controllers/user_comments_controller.rb

### 雛形
    class コントローラ名Controller < ApplicationController
      def メソッド名
      end
    edn