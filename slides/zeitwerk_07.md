### Zeitwerk

* Zeitwerkを使用したcode loaderの登場によりcode loaderが2種類になった
* デフォルトでは元のcode loader(classic autoloaderと呼ばれている)
* Zeitwerkを使用するにはload_defaultsに6.0を指定する or config.autoloaderに:zeitwerkを指定する
  * ZeitwerkはJRuby未サポートらしく、JRubyの場合load_defaultsに6.0を指定してもclassic autoloaderが使用される
