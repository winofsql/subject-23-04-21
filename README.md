# subject-23-04-21

```javascript
function myFunction() {

  // 以下のコードは、現在の日付と時刻を電子メールで送信します。
  var now = new Date();
  GmailApp.sendEmail("", "突然すみません", "こんにちは\nさようなら");  
  
}

// function sendEmail() {
//   var sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
//   var recipient = sheet.getRange("A2").getValue();
//   var subject = sheet.getRange("B2").getValue();
//   var body = sheet.getRange("C2").getValue();

//   GmailApp.sendEmail(recipient, subject, body);
// }

function sendEmail() {
  try {
    var sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
    var recipient = sheet.getRange("A2").getValue();
    var subject = sheet.getRange("B2").getValue();
    var body = sheet.getRange("C2").getValue();

    if (recipient && subject && body) {
      GmailApp.sendEmail(recipient, subject, body);
      Logger.log("メールを送信しました。");
    } else {
      throw new Error("送信先、件名、本文のいずれかが未入力です。");
    }
  } catch (error) {
    Logger.log("エラーが発生しました: " + error);
  }
}
```
