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

このスクリプトでは、`sendEmail` 関数を定義しています。`recipient`、`subject`、および `body` 変数を設定して、メールの送信先、件名、および本文を指定します。`GmailApp.sendEmail` メソッドを使用して、メールを送信します。

上記のスクリプトを使用する場合、スクリプトエディタで関数を実行することで、指定したメールアドレスにメールが送信されます。

上記の例をベースに、必要に応じて送信元、添付ファイル、HTML フォーマットなどの追加機能を組み込むこともできます。また、スプレッドシートやフォームなど、他の Google アプリケーションと統合することもできます。

<br><br>

### スプレッドシートに入力した内容を使って GAS でメール送信するプログラムを作成してください

スプレッドシートに入力された内容を使用してメールを送信するプログラムを作成することができます。以下は、スプレッドシートに入力された内容を取得し、メールを送信するスクリプトの例です。

```javascript
function sendEmail() {
  var sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
  var recipient = sheet.getRange("A2").getValue();
  var subject = sheet.getRange("B2").getValue();
  var body = sheet.getRange("C2").getValue();

  GmailApp.sendEmail(recipient, subject, body);
}
```

このスクリプトでは、`sendEmail` 関数を定義しています。`SpreadsheetApp.getActiveSpreadsheet().getActiveSheet()` メソッドを使用して、現在アクティブなスプレッドシートを取得し、`getRange` メソッドを使用して、`A2`、`B2`、および `C2` のセルから、それぞれメールの送信先、件名、および本文を取得しています。そして、`GmailApp.sendEmail` メソッドを使用して、メールを送信します。

上記のスクリプトを使用する場合、スプレッドシートに送信先、件名、および本文を入力し、スクリプトエディタで関数を実行することで、指定したメールアドレスにメールが送信されます。

また、スプレッドシートに複数の行がある場合は、ループを使用して、各行に対してメールを送信することもできます。また、スプレッドシートから添付ファイルを取得して、メールに添付することもできます。
