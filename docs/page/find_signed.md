---
layout: page
---

### 説明

有効期限付きの署名されたIDからレコードを取得

### 使い方

    モデル.find_signed(署名されたID, purpose: nil)

    # 失敗したら例外発生
    モデル.find_signed!(署名されたID, purpose: nil)

### 例

    signed_id = User.first.signed_id expires_in: 15.minutes, purpose: :password_reset

    User.find_signed signed_id #=> nil, since the purpose does not match

    travel 16.minutes
    User.find_signed signed_id, purpose: :password_reset #=> nil, since the signed id has expired

    travel_back
    User.find_signed signed_id, purpose: :password_reset #=> User.first

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/signed_id.rb#L42)
