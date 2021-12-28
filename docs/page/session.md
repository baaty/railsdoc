---
layout: page
---

### 説明

セッションに情報を保存

### 使い方

    session[キー] = 値

### 例

#### セッションに情報を保存

    session[:user_name] = 'test'

#### @userがnilかfalseだったら代入

    @user ||= User.find(session[:user_id])
