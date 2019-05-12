### Zeitwerk

* 名前解決の挙動が違うので、classic autoloaderとzeitwerk autoloaderは完全に互換性があるわけではない
* アプリの構造がzeitwerk autoloaderで正しくロード出来るかどうかをチェックする為のタスクが提供されている

```
$ bin/rails zeitwerk:check
```
