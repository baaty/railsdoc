---
layout: archive_page
---
### 説明
ActiveRecordを使って指定した条件のレコードを削除  
dependentが設定されている場合は関連付けられたモデルも削除

### 使い方
    モデル.destroy([条件])

### 例
#### 指定した条件のレコードを削除
   person.pets.destroy(Pet.find(1))

#### 複数指定
    person.pets.destroy(Pet.find(2), Pet.find(3))

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/associations/collection_proxy.rb#L692)