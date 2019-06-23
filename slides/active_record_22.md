#### [Add collection cache versioning](https://github.com/rails/rails/commit/4f2ac80d4cdb01c4d3c1765637bed76cc91c1e35)

* Activ Record Relationでもrecyclable cache keyが出来るようになったよ
  * ActiveRecord::Relation#cache_keyが返すkeyにはrecordのcountやtimestampは含まれないようになった
* デフォルトでは無効化されており、ActiveRecord::Base.collection_cache_versioningにtrueを指定した場合のみ有効化される
