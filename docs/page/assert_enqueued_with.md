---
layout: page
---

### 説明

指定した引数でジョブを登録されているか確認

### 使い方

    assert_enqueued_with(job: ジョブ=nil, args: 引数=nil, at: At=nil, queue: キュー=nil, priority: プライオリティ=nil, ブロック引数)

### 例

#### 指定した引数でジョブを登録

    MyJob.perform_later(1,2,3)
    assert_enqueued_with(job: MyJob, args: [1,2,3], queue: 'low')

#### ジョブに渡す引数を指定

    MyJob.perform_later(foo: 'bar', other_arg: 'No need to check in the test')
    assert_enqueued_with(job: MyJob, args: expected_args, queue: 'low')

#### ブロックで渡す

    assert_enqueued_with(job: MyJob, args: [1,2,3], queue: 'low') do
      MyJob.perform_later(1,2,3)
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activejob/lib/active_job/test_helper.rb#L392)
