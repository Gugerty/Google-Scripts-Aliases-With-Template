# Google Script Aliases with HTML


> This is a simple but powerful Google Script that uses one of your alias email accounts you've setup either on regular **G-Mail** or **G-Suite**.

### Usage:

To use this script, either visit this **[LINK](https://script.google.com/d/13D_hVRMjz5ld3Mgh93qmSag1uwbJxlU6XFKI_oBHswhqQSJCpNbwsv5y/edit?usp=sharing)**  and under **File** select **Make a copy**, or just copy the code below into your Script Project.

Be sure and link your HTML template properly with the correct name if you don't just clone the example.

Additionally I included an Email template you are free to use and modify! 🤗

```javascript
function aliasMailApp() {
  var template = HtmlService.createTemplateFromFile("template.html");
  var aliases = GmailApp.getAliases();
  GmailApp.sendEmail(
/* / RECIPIENT / */  'recipient@address.com',
/* EMAIL SUBJECT */  "Subject line content goes here.",
/* / HTML BODY / */  '', {
/* ///////////// */  htmlBody: template.evaluate() .getContent(),
/*  FROM / ALIAS */     'from': aliases[0]
/* ///////////// */      }
/* ///////////// */  );
}
```



## Email Template:

![alt text](https://i.imgur.com/Xaa7qtn.jpg "Example Email Template for Implimentation")

This Email Template is free to be used and modified! Enjoy! 😎

## Author

👤 **Sean Gugerty**

* Website: https://www.seangugerty.press
* Github: [@Gugerty](https://github.com/Gugerty)
*LinkedIn:  [LinkedIn](https://www.linkedin.com/in/seangugerty)

## Show your support

Give a ⭐️ if this project helped you!

***
