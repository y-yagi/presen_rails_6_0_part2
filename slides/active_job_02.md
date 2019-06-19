#### [Add support for custom serializers for Active Job arguments](https://github.com/rails/rails/pull/30941)

* jobの引数に任意のオブジェクトを渡せるようにするための仕組み
  * 元々はRails側で管理されているクラス(String、Active Recordのmodel、HashWithIndifferentAccess等々)のオブジェクトしかjobの引数にしか渡せなかったので、使用出来る引数に制限があった
* 独自のクラスのオブジェクトを渡したい場合、そのオブジェクトのserialize / deserialize処理を定義した独自のserializerクラスを作成する必要がある
  * ActiveJob::Serializers::ObjectSerializerがserialize / deserialize処理の為の基本クラスなので、それを継承したクラスを作成する
