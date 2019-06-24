#### [Action Cable Testing](https://github.com/rails/rails/pull/33659)

* Action Cableの単体テストの為の仕組み
* Action Cableに関するテストはブラウザを使用して行うテスト(現在のシステムテスト)で行った方がよく、単体テストは必要は無いのではという、意見があって単体テストの為の仕組みがなかなか導入されなかった
* が、API-onlyアプリケーションでAction Cableを使いたいんだけど、テストどうしたらよいの、というissueがきて晴れて導入された
