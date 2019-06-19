#### [Introduce `ActionDispatch::ActionableExceptions`](https://github.com/rails/rails/pull/34788)

* これ書いている時点では PendingMigrationErrorにだけ対応
  * Active Storage、Action Mailbox等のセットアップ不足でエラーになった場合も対応出来るようになる予定
  * [Hook up the new frameworks with Actionable Error](https://github.com/rails/rails/pull/36455)
