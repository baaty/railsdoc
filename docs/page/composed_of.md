---
layout: page
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
:allow_nil   | nilの検証をスキップ
:constructor | 条件
:converter   | 新しい値が値オブジェクトに割り当てられたときに呼び出される

### 例
#### 複数カラムを擬似的に1つにまとめる
    composed_of :temperature, mapping: %w(reading celsius)

#### マッピング指定
    composed_of :balance, class_name: "Money", mapping: %w(balance amount), converter: Proc.new { |balance| balance.to_money }

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/aggregations.rb#L223)