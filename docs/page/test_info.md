---
layout: page
---

### 説明

- あるURLにアクセスした際に、予期した画面が表示されるか
- ある正しい操作をした際に、アプリケーションの状態が正しく変更されるか
- ある正しくない操作をした際に、適切なエラーメッセージが表示されるか

### 単体テスト

- モデルの検索系メソッドが正しい値を取得できるか
- モデルの更新系メソッドが正しくデータベースを更新できるか
- モデルの更新系メソッドが不正な入力に対して、適切なエラーを発生させるか

### 機能テスト

- 適切なテンプレートが選択されているか
- インスタンス変数に適切な値が格納されているか
- 適切にレンダリングされているか
- 更新系のアクションが正しくデータベースを更新されるか

### 総合テスト

- ログインして、新しいメンバーを追加して、ログアウトするといった一連の動きをテスト
