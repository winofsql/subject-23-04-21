# subject-23-04-21(金)

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

![image](https://user-images.githubusercontent.com/1501327/233643255-46729d33-5a42-4aac-8a8a-9b474f92bd8c.png)

![image](https://user-images.githubusercontent.com/1501327/233650146-32d206c5-9427-4d05-aec0-eedddf44bb43.png)

![image](https://user-images.githubusercontent.com/1501327/233650530-092a4352-ab0d-4e98-afb6-52248bb3a2e1.png)

![image](https://user-images.githubusercontent.com/1501327/233651314-bc52de0f-6535-4287-b9b0-c4caa6c629c6.png)

```cs
namespace cs_0421_02;

partial class Form1
{
    /// <summary>
    ///  Required designer variable.
    /// </summary>
    private System.ComponentModel.IContainer components = null;

    /// <summary>
    ///  Clean up any resources being used.
    /// </summary>
    /// <param name="disposing">true if managed resources should be disposed; otherwise, false.</param>
    protected override void Dispose(bool disposing)
    {
        if (disposing && (components != null))
        {
            components.Dispose();
        }
        base.Dispose(disposing);
    }

    #region Windows Form Designer generated code

    /// <summary>
    ///  Required method for Designer support - do not modify
    ///  the contents of this method with the code editor.
    /// </summary>
    private void InitializeComponent()
    {
        this.components = new System.ComponentModel.Container();
        this.AutoScaleMode = System.Windows.Forms.AutoScaleMode.Font;
        this.ClientSize = new System.Drawing.Size(800, 450);
        this.Text = "Form1";

        // テキストボックスの作成と設定
        this.textBox1 = new System.Windows.Forms.TextBox();
        this.textBox1.Location = new System.Drawing.Point(50, 50);
        this.textBox1.Size = new System.Drawing.Size(200, 25);
        this.textBox1.Text = "";

        // フォームにテキストボックスを追加
        this.Controls.Add(this.textBox1);
    }

    TextBox textBox1;

    #endregion
}
```
