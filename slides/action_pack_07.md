#### [Introduce `ActionDispatch::ActionableExceptions`.](https://github.com/rails/rails/pull/34788)

* これ書いている時点では PendingMigrationErrorにだけ対応している
  * Active Storage、Action Mailbox等のセットアップでエラーになった場合にも対応出来るようにする予定
  * [Hook up the new frameworks with Actionable Error](https://github.com/rails/rails/pull/36455)
