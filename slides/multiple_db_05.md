### multiple DB

* レプリカに対して書き込みを実行するとエラーになる
  * レプリカかどうかは設定ファイルのreplica keyで決まる

```ruby
ActiveRecord::Base.connected_to(database: :primary_replica) { User.create! }
# => ActiveRecord::ReadOnlyError (Write query attempted while in readonly mode: INSERT INTO "users" ("created_at", "updated_at") VALUES (?, ?))
```
