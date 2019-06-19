#### [Add support for setting Optimizer Hints on databases](https://github.com/rails/rails/pull/35615)

* Optimizer Hintsを指定する為のメソッド

```ruby
# MySQL

Topic.optimizer_hints("MAX_EXECUTION_TIME(50000)", "NO_INDEX_MERGE(topics)")
# SELECT /*+ MAX_EXECUTION_TIME(50000) NO_INDEX_MERGE(topics) */ `topics`.* FROM `topics`

# PostgreSQL(pg_hint_plan)

Topic.optimizer_hints("SeqScan(topics)", "Parallel(topics 8)")
# SELECT /*+ SeqScan(topics) Parallel(topics 8) */ "topics".* FROM "topics"
```

* MySQLは本体でサポートされているが、PostgreSQLの場合は別途[pg\_hint\_plan](http://pghintplan.osdn.jp/pg_hint_plan-ja.html) moduleのインストールが必要
