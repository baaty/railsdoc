---
layout: page
---
### 説明
複数カラムを擬似的に1つにまとめる

### 使い方
    モデル.composed_of(条件, オプション)

### オプション

オプション        | 説明
------------ | -------------------
:class_name  | クラス名
:mapping     | マッピング
:allow_nil   | trueならば、nilの検証はスキップ
:constructor | 条件
:converter   |

### 例
    composed_of :temperature, mapping: %w(reading celsius)
    composed_of :balance, class_name: "Money", mapping: %w(balance amount), converter: Proc.new { |balance| balance.to_money }
    composed_of :address, mapping: [ %w(address_street street), %w(address_city city) ]
    composed_of :gps_location
    composed_of :gps_location, allow_nil: true
    composed_of :ip_address, class_name: 'IPAddr', mapping: %w(ip to_i), constructor: Proc.new { |ip| IPAddr.new(ip, Socket::AF_INET) }, converter: Proc.new { |ip| ip.is_a?(Integer) ? IPAddr.new(ip, Socket::AF_INET) : IPAddr.new(ip.to_s) }

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/08576b94ad4f19dfc368619d7751e211d23dcad8/activerecord/lib/active_record/aggregations.rb#L212)