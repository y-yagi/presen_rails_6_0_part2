#### [Introduce `ActionDispatch::ActionableExceptions`](https://github.com/rails/rails/pull/34788)

* Rails標準のエラー画面でエラー内容に応じたアクションを実行出来るようにする為の仕組み
  * ActiveRecord::PendingMigrationError が発生した場合に、エラー画面からdb:migrateが実行出来る
  * ![エラー画面](https://user-images.githubusercontent.com/604618/50423897-7093d880-0864-11e9-9211-26056016fe5b.png)
