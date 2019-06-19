#### [Replace existing images instead of adding to them when updating an attached model via `update` or `update!` with, say, `@user.update!(images: [ … ]](https://github.com/rails/rails/pull/33303)

* これにより、update時の挙動がファイルの追加から置き換えに変更になった(非互換)
* フラグで古い挙動になるようにすべきだよね、という話があるがまだ未対応
  * [Active Storage has_many_attached attachments get destroyed when subsequent files are attached](https://github.com/rails/rails/issues/36374)
