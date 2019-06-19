#### [Add a configuration option to customize format of the `ActiveModel::Errors#full_message`](https://github.com/rails/rails/pull/32956)

* ActiveModel::Errors#full_messageメソッドで出力エラーのフォーマットを変更出来るよう対応
* 元々、:"errors.format"で上書き出来るようになっていたが、これは全体に影響がある設定で、attribute個別の上書きは出来なかった
* この対応で上記以外のkeyでフォーマットの上書きが出来るようになりました
