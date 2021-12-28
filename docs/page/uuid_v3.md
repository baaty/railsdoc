---
layout: page
---

### 説明

Digest::MD5を使ったUUID

### 使い方

    Digest::UUID.uuid_v3(UUIDの名前空間, 名前)

### 例

    Digest::UUID.uuid_v3("name_space", "sample")
    # "3b0ead59-ca8d-350b-a392-e656db58b0fc"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activesupport/lib/active_support/core_ext/digest/uuid.rb#L44)
