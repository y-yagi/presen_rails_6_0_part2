#### [Add support for multi environment credentials](https://github.com/rails/rails/pull/33521)

* env毎のcredentials、及び、keyはconfig/credentialsディレクトリ配下に生成される
  * envがproductionの場合はproduction.key、及び、production.yml.enc
  * keyを環境変数で指定したい場合は、既存のcredentials同様RAILS_MASTER_KEYで指定可能(環境変数はenv問わず同じ)
* なお、credentialファイルは、env毎のcredentialファイル -> 共通のcredentialファイル(config/credentials.yml.enc)の順で検索されるようになっており、先に見つかったファイルが使用される
  * 内容のmergeは行われないので、env毎のcredentialファイルが使用される場合config/credentials.yml.encはロードされない
