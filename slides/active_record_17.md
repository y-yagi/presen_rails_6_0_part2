#### [Make it possible to override the implicit order column](https://github.com/rails/rails/pull/34480)

* firstやlastのようなordered finder methodsでorderに使用するカラムを指定出来るようになった

```ruby
class User < ActiveRecord::Base
  self.implicit_order_column = "created_at"
end
```

```ruby
User.first
# =>User Load (0.2ms)  SELECT "users".* FROM "users" ORDER BY "users"."created_at" ASC LIMIT ?  [["LIMIT", 1]]
```

* primary keyにUUIDのようなauto-incrementing integerじゃない値を使用している場合に、primary keyでorderされても結果は期待通りにならない(firstを使用しても最初の値は取得出来ない)為、そのような場合に任意のカラムでorder出来るようにする為
