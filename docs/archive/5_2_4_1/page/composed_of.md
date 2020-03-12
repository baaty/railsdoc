---
layout: archive_page
---
### 説明
複数カラムを擬似的に1つにまとめる

### 使い方
    モデル.composed_of(条件 [, オプション])

### オプション

オプション        | 説明
------------ | -------------------
:class_name  | クラス名
:mapping     | マッピング
:allow_nil   | nilのバリデーションをスキップ
:constructor | 条件
:converter   | 新しい値が値オブジェクトに割り当てられたときに呼び出される

### 例
#### 複数カラムを擬似的に1つにまとめる
    composed_of :temperature, mapping: %w(reading celsius)

#### マッピング指定
    composed_of :balance, class_name: "Money", mapping: %w(balance amount), converter: Proc.new { |balance| balance.to_money }

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/aggregations.rb#L225)