---
layout: page
---

### 説明

Digest::SHA1を使ったUUID

### 使い方

    Digest::UUID.uuid_v5(UUIDの名前空間, 名前)

### 例

    Digest::UUID.uuid_v5("name_space", "sample")
    # "d7a9ae1a-b099-5318-8828-340cc10a1550"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activesupport/lib/active_support/core_ext/digest/uuid.rb#L49)
