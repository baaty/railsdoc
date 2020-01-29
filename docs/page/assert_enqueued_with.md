---
layout: page
---
### 説明
指定した引数でジョブを登録

### 使い方
    assert_enqueued_with([job: ジョブ名, args: 引数, at: nil, queue: キュー])

### 例
    MyJob.perform_later(1,2,3)
    assert_enqueued_with(job: MyJob, args: [1,2,3], queue: 'low')

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activejob/lib/active_job/test_helper.rb#L382)