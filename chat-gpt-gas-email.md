### GAS でメール送信するプログラムを作成してください

Google Apps Script (GAS) を使用して、Gmail を使用してメールを送信するプログラムを作成することができます。以下は、基本的なメール送信スクリプトの例です。

```javascript
function sendEmail() {
  var recipient = "送信先メールアドレス";
  var subject = "メールの件名";
  var body = "メールの本文";

  GmailApp.sendEmail(recipient, subject, body);
}
```
