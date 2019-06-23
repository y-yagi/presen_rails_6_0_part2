#### [Add attachment and attachments field generators](https://github.com/rails/rails/pull/35805)

* generatorにattachment、attachments fieldを指定出来るようになった
* Active Storage用のfieldで、指定するとmodelへのhas_one_attached、又は、has_many_attachedの追加、formへのfield_filed等の追加を行ってくれる
* 同様に、Action Text用のrich_text fieldが追加されている
  * [Add rich_text field to model generators](https://github.com/rails/rails/pull/35781)
