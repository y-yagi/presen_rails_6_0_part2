#### [Add insert_all to ActiveRecord models](https://github.com/rails/rails/pull/35077)

* usert_allは名前の通りでUPSERT(PostgreSQL / SQLiteでは`ON CONFLICT`、MySQLでは`ON DUPLICATE KEY UPDATE`)が使用されるようになってる　
  * 当然DBはそれらの機能の使用出来るバージョン以上である必要がある

```ruby
User.upsert_all([
  { id: 1, name: 'a', created_at: Time.current, updated_at: Time.current },
  { id: 2, name: 'b', created_at: Time.current, updated_at: Time.current },
])

User.upsert_all([
  { id: 1, name: 'a', created_at: Time.current, updated_at: Time.current },
  { id: 2, name: 'b', created_at: Time.current, updated_at: Time.current },
])
# => INSERT INTO "users"("id","name","created_at","updated_at") VALUES (1, 'a', '2019-06-16 07:36:38.699495', '2019-06-16 07:36:38.699507'), (2, 'b', '2019-06-16 07:36:38.699510', '2019-06-16 07:36:38.699513') ON CONFLICT ("id") DO UPDATE SET "name"=excluded."name","created_at"=excluded."created_at","updated_at"=excluded."updated_at" RETURNING "id"
```
