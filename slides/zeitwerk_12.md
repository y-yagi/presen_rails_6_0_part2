### Zeitwerk

* cache_classes = trueの場合reload処理は動作しない(エラーになる)
* 元々config/environments/test.rbではache_classes = trueだったが、これだとSpringを使用している場合に問題がおきる
  * Springがコードをreloadするが上記制限によりエラーになる
* テスト環境でSpringを使用している場合cache_classes = falseを指定する必要がある
  * generate config.cache_classes = false if Spring https://github.com/rails/rails/commit/65344f254cde87950c7f176cb7aa09c002a6f882
