### 設定ファイル例

```yml
development:
  primary:
    <<: *default
    database: db/my_primary_db.sqlite3
  primary_replica:
    <<: *default
    database: db/my_primary_replica_db.sqlite3
    replica: true
  animals:
    <<: *default
    database: db/animals.sqlite3
    migrations_paths: "db/animals_migrate"
```
