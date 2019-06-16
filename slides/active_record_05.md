#### [Add insert_all to ActiveRecord models](https://github.com/rails/rails/pull/35077)

* bulk insert用のinsert_all / insert_all! / upsert_allメソッドを追加
  * callback、validationは実行されないので、callbackで設定している値は明示的に指定する必要がる
  * created_at / updated_atも注意が必要

```ruby
User.insert_all!([
  { name: 'a', created_at: Time.current, updated_at: Time.current },
  { name: 'b', created_at: Time.current, updated_at: Time.current },
  { name: 'c', created_at: Time.current, updated_at: Time.current }
])
```
