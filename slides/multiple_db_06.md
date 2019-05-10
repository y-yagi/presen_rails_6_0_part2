### multiple DB

* adapter毎に"READ"とみなすQUERYを定義して、それ以外は全て書き込み処理とみなすようにしている
  * https://github.com/rails/rails/blob/3363a3c2a54ab1796f1a520538820271f977bc71/activerecord/lib/active_record/connection_adapters/sqlite3/database_statements.rb#L7
  * https://github.com/rails/rails/blob/3363a3c2a54ab1796f1a520538820271f977bc71/activerecord/lib/active_record/connection_adapters/mysql/database_statements.rb#L22
  * https://github.com/rails/rails/blob/3363a3c2a54ab1796f1a520538820271f977bc71/activerecord/lib/active_record/connection_adapters/postgresql/database_statements.rb#L70
