---
layout: page
---

### 説明

ラックベースのアプリケーションをマウント

### 使い方

    mount(アプリケーション, オプション=nil)

### オプション

| オプション           | 説明                                                              |
| -------------------- | ----------------------------------------------------------------- |
| :controller, :action | コントローラとアクションを指定。必ずセットで指定                  |
| :to                  | :controller, :actionの短縮形。#でコントローラとアクションを区切る |
| :param               | パラメータを指定                                                  |
| :path                | パスを指定                                                        |
| :module              | コントローラの名前空間                                            |
| :as                  | ルート名に使用する別名                                            |
| :via                 | HTTPメソッドを指定                                                |
| :on                  | 名前付きルートを指定                                              |
| :constraints         | URLのフォーマットを制限                                           |
| :defaults            | デフォルト値                                                      |
| :anchor              | アンカーリンク                                                    |
| :format              | フォーマットを指定                                                |

### 例

    mount SomeRackApp, at: "some_route"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/routing/mapper.rb#L588)
