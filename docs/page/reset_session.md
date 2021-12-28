---
layout: page
---

### 説明

セッション情報を削除

### 使い方

#### すべて

    reset_session

#### 一部

    session[キー] = nil

### 例

#### すべてのセッション情報を削除

    reset_session

#### user_nameのセッション情報を削除

    session[:user_name] = nil
