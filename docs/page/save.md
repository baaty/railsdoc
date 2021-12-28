---
layout: page
---

### 説明

生成したモデルオブジェクトをデータベースに保存

### 使い方

    モデル.save(オプション引数)

    # 失敗したら例外発生
    モデル.save!(オプション引数)

### 例

#### 生成したモデルオブジェクトをデータベースに保存

    user = User.new
    user.name = "A"
    user.save

#### 新しいローカル変数を作らずに保存

    User.new do |i|
      i.name = "A"
      i.save
    end

#### 属性ハッシュの保存

    user = User.new(name: "A")
    user.save

#### データベースへの保存の有無で処理を分ける

    if @user.save
      redirect_to :list
    else
      render action: "new"
    end

#### 複数の項目を保存

    begin
      Entry.transaction do
        @many_entries.each { |entry| entry.save! }
      end
     vredirect_to :list
      rescue ActionRecord::RecordInvalid, ActionRecord::RecordNotSaved: ex
      render action: "input_multi_entries"
    end

#### 属性を変更して保存

    @entry = Entry.find(params[:id])
    @entry.message = "new Message"
    @entry.save

#### 複数の項目を1度に更新

    @user = User.find(parms[:id])
    @user.attributes = { username: 'Phusion', is_admin: true }
    @user.save

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/persistence.rb#L615)
