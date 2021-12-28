---
layout: page
---

### 説明

数値をパーセントに変換

### 使い方

    number_to_percentage(数値, オプション={})

### オプション

| オプション                 | 説明                         | デフォルト                        |
| -------------------------- | ---------------------------- | --------------------------------- |
| :locale                    | 使用するロケール             | current locale                    |
| :precision                 | 小数以下の桁数               | 3                                 |
| :signigicant               | 全体桁数                     | false                             |
| :separator                 | 小数点記号                   | .                                 |
| :delimiter                 | 桁区切り文字                 |                                   |
| :strip_insignidicant_zeros | 小数点以下の0を削除          | false                             |
| :format                    | 出力される文字のフォーマット | %u%n(%uは通貨の単位 %nは数字部分) |
| :raise                     | エラーの場合に例外           |                                   |

### 例

    number_to_percentage(100)
    # 100.000%

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/number_helper.rb#L167)
