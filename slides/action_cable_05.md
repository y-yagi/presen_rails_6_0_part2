#### [Convert the Action Cable JavaScript package from CoffeeScript to ES2015 and publish the source code in the npm distribution](https://github.com/rails/rails/pull/34370)

* Action CableのソースがCoffeeScriptで書かれていたのをES2015に変換
* この対応の影響で一部APIに非互換が発生している
  * 詳細は https://edgeguides.rubyonrails.org/upgrading_ruby_on_rails.html#action-cable-javascript-api-changes を見てね
* 因みにrails-ujsはまだCoffeeScript(JavaScriptへの移行予定はある)
