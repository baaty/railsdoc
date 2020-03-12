---
layout: archive_page
---
### 説明
セッションに情報を保存

### 使い方
    session[キー] = 値

### 例
#### 基本形(オプションなし)
    session[:user_name] = 'test'

#### @userがnilかfalseだったら、@userにUser.find(session[:user_id])を代入
    @user ||= User.find(session[:user_id])