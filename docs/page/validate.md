---
layout: page
---

### 説明

バリデーションを定義

### 使い方

    validate(バリデーションメソッド名.., ブロック引数)

    # 失敗したら例外発生
    validate!(バリデーションメソッド名.., ブロック引数)

### オプション

| オプション   | 説明                           | デフォルト値 |
| ----------- | ----------------------------- | ----------- |
| :on          | 実行するタイミング             | 保存時       |
| :allow_nil   | nilをスキップ                  | false        |
| :allow_blank | nilや空文字をスキップ          | false        |
| :if          | バリデーションする条件を指定   |              |
| :unless      | バリデーションしない条件を指定 |              |
| :strict      | 失敗した場合に例外を発生       |              |

### 例

#### バリデーションを定義

    validate :must_be_friends

#### ブロック

    validate do |comment|
      comment.must_be_friends
    end

### ソースコード

- [GitHub]()
