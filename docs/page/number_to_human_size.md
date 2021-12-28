---
layout: page
---

### 説明

バイト単位の数値を変換

### 使い方

    number_to_human_size(数値, オプション={})

### オプション

| オプション                 | 説明                | デフォルト値 |
| -------------------------- | ------------------- | ------------ |
| :locale                    | 使用するロケール    | locale       |
| :precision                 | 小数以下の桁数      | 3            |
| :signigicant               | 全体桁数            | true         |
| :separator                 | 小数点記号          | .            |
| :delimiter                 | 桁区切り文字        |              |
| :strip_insignidicant_zeros | 小数点以下の0を削除 | true         |
| :raise                     | エラーの場合に例外  |              |

### 例

#### バイト単位に変換

    number_to_human_size 123456789
    # 118 MB

#### 小数以下の桁数を指定

    number_to_human_size 524288000, precision: 5
    # 500 MB

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/number_helper.rb#L297)
