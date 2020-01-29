---
layout: page
---
### 説明
指定した個数のジョブが登録さているか確認

### 使い方
    assert_enqueued_jobs(個数 [, only: nil, except: nil, queue: nil])

### 例
    assert_enqueued_jobs 0
    HelloJob.perform_later('david')
    assert_enqueued_jobs 1
    HelloJob.perform_later('abdelkader')
    assert_enqueued_jobs 2

    assert_enqueued_jobs 1 do
      HelloJob.perform_later('cristian')
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activejob/lib/active_job/test_helper.rb#L120)