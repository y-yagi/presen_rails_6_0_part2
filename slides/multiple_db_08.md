### multiple DB

* `connects_to`にはロールとDB名のペアを指定する
  ```ruby
  connects_to database: { writing: :animals }
  ```

* DB名は設定ファイルで記載した名前
* ロールは接続先を識別するための値
  * 任意の値を指定でき、その値をconnected_toに指定出来る
