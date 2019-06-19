#### [Action Cable Testing](https://github.com/rails/rails/pull/33659)

* Action Cableのテストの為の仕組み
* Action Cableに関するテストはブラウザを使用して行うテスト(現在のシステムテスト)で確認した方が正確で、単体でテストは行う必要は無いのではという、意見があってテストの為の仕組みがなかなか導入されなかった
* API-onlyアプリケーションでAction Cableを使いたいんだけど、テストどうしたらよいねん、というissueがきて晴れて導入された
