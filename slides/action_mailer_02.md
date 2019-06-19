#### [Add `MailDeliveryJob` for delivering both regular and parameterized mail](https://github.com/rails/rails/pull/34591)

* Action Mailerでメール送信に使われるjobクラスが通常のメールとparameterizedメールでわかれていたのを1つにしましょう、という対応
  * ActionMailer::DeliveryJobとActionMailer::Parameterized::DeliveryJobが使われていたが、今後はActionMailer::MailDeliveryJob
* 古い方のクラスはdeprecatedになっているので、新しい方を使うようにしてください
