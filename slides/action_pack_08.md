#### [Introduce guard against DNS rebinding attacks](https://github.com/rails/rails/pull/33145)

* DNS Rebinding攻撃やHostヘッダー攻撃の対策用のmiddleware(ActionDispatch::HostAuthorization)を追加
* 認証はホワイトリスト方式で、登録されていないホスト以外へのリクエストはエラーになる
  * デフォルトではdevelopment環境での値(`IPAddr.new("0.0.0.0/0")`、`IPAddr.new("::/0")`、`localhost`)が指定されており、その他の環境では空(チェックが行われない状態)
* ホストを追加したい場合は、Rails.application.config.hostsに値を指定する(e.g. Rails.application.config.hosts << "product.com")
