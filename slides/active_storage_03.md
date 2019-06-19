#### [Replace existing images instead of adding to them when updating an attached model via `update` or `update!` with, say, `@user.update!(images: [ … ]](https://github.com/rails/rails/pull/33303)

* 新規にアップロードしたファイルが、オブジェクトにアサインされた際に即座に保存されていたのを、そのアサインしたオブジェクトがsaveされた後に保存するよう変更

```ruby
@user.avatar = params[:avatar]
```

* 上記のようなコードで、Rails 5.2ではアサインされた際に即座にファイルが保存されてしましたが、6.0では@userのsaveが成功した後にファイルが保存されるようになった
  * ファイル設定 / 保存の間にバリデーションを挟めるようにする為、だったはずがバリデーション機能は結局まだ入らなかった
