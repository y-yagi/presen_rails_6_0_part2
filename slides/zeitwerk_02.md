### Zeitwerk

* 元々のcode loaderはconst_missingを元にした実装になっていた
* ただ、const_missingだとネスト等の情報が取得出来ず、Rubyのload処理と異なる挙動になっていた
  * ネストしたクラス / モジュールを定義する際に問題になっていた
