#### [Deprecate `update_attributes` and `update_attributes!`](https://github.com/rails/rails/pull/31998)

* update_attributes、及び、update_attributes!メソッドが正式にdeprecateになった
  * 今後は`update`、`update!`メソッドを使用してね
* 元々`update`、`update!`メソッド追加された際([Rename update_attributes method to update](https://github.com/rails/rails/pull/8705))に`update_attributes(!)`は"soft deprecation" という扱いになっていた
  * "そろそろ正式にdeprecateにしても良いんじゃね"という意見が出た為deprecateになりました
