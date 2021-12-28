---
layout: page
---

### 説明

クライアントに送信する前にクッキーの値を自動的に暗号化し、読み取り時には復号化するjarを返す  
クッキーがユーザ(または第三者)によって改ざんされていた場合はnil

### 使い方

    cookies.encrypted[クッキー名] = 値

### 例

    cookies.encrypted[:discount] = 45
    #=> Set-Cookie: discount=DIQ7fw==--K3n//8vvnSbGq9dA--7Xh91HfLpwzbj1czhBiwOg==; path=/
    cookies.encrypted[:discount] #=> 45

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/middleware/cookies.rb#L249)
