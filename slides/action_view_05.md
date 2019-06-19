#### Refactoring Action View

* テンプレートレンダリング周りのリファクタリング諸々
* そもそもdev環境でメモリリークが発生している、という問題があり、この対策してのリファクタリング
  * [Rails development mode memory leak and slowdown, also on new apps](https://github.com/rails/rails/issues/32892)
  * (関係ない修正も含まれているきもするが)
* Railsアプリの開発者は影響無い(はず)
  * Action Viewを拡張するgemは影響ありますので、よしなに
