#### [Add insert_all to ActiveRecord models](https://github.com/rails/rails/pull/35077)

* insert_all!はunique constraintに違反した場合ActiveRecord::RecordNotUniqueをraiseするようになっている
  * insert_allは無視(実行するクエリーが違う)

```ruby
User.insert_all([
  { id: 1, name: 'a', created_at: Time.current, updated_at: Time.current },
  { id: 1, name: 'b', created_at: Time.current, updated_at: Time.current },
])
# => INSERT INTO "users"("id","name","created_at","updated_at") VALUES (1, 'a', '2019-03-05 23:10:02.382965', '2019-03-05 23:10:02.382977'), (1, 'b', '2019-03-05 23:10:02.382980', '2019-03-05 23:10:02.382983') ON CONFLICT  DO NOTHING RETURNING "id"

User.insert_all!([
  { id: 1, name: 'a', created_at: Time.current, updated_at: Time.current },
  { id: 1, name: 'b', created_at: Time.current, updated_at: Time.current },
])
# => INSERT INTO "users"("id","name","created_at","updated_at") VALUES (1, 'a', '2019-06-19 05:01:17.922194', '2019-06-19 05:01:17.922217'), (1, 'b', '2019-06-19 05:01:17.922224', '2019-06-19 05:01:17.922227') RETURNING "id"
# => ActiveRecord::RecordNotUnique (PG::UniqueViolation: ERROR:  重複キーが一意性制約"users_pkey"に違反しています)
```
