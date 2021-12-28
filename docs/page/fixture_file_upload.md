---
layout: page
---

### 説明

ファイルアップロードをテスト

### 使い方

    fixture_file_upload(パス, タイプ=nil, バイナリかどうか=false)

### 例

    post :change_avatar, params: { avatar: fixture_file_upload('david.png', 'image/png') }

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/testing/test_process.rb#L19)
