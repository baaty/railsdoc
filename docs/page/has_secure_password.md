---
layout: page
---

### 説明

BCryptパスワードを設定して認証するためのメソッド

### 使い方

    has_secure_password(属性=:password, validations: バリデーション=true)

### 例

    class User < ActiveRecord::Base
        has_secure_password
        has_secure_password :recovery_password, validations: false
    end
    user = User.new(name: 'david', password: '', password_confirmation: 'nomatch')
    user.save                                                  #=> false, password required
    user.password = 'mUc3m00RsqyRe'
    user.save                                                  #=> false, confirmation doesn't match
    user.password_confirmation = 'mUc3m00RsqyRe'
    user.save                                                  #=> true
    user.recovery_password = "42password"
    user.recovery_password_digest                              #=> "$2a$04$iOfhwahFymCs5weB3BNH/uXkTG65HR.qpW.bNhEjFP3ftli3o5DQC"
    user.save                                                  #=> true
    user.authenticate('notright')                              #=> false
    user.authenticate('mUc3m00RsqyRe')                         #=> user
    user.authenticate_recovery_password('42password')          #=> user
    User.find_by(name: 'david')&.authenticate('notright')      #=> false
    User.find_by(name: 'david')&.authenticate('mUc3m00RsqyRe') #=> user

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/secure_password.rb#L61)
