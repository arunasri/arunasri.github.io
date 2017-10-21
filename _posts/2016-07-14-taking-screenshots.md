---
layout: post
title:  Taking screenshots using java
tags:
- Selenium WebDriver
- Java
- Screenshot
---
## Use below code to take screenshots in our java selenium
```java
File scrFile = ((TakesScreenshot) driver).getScreenshotAs(OutputType.FILE);
FileUtils.copyFile(scrFile, new File("awesomepicture.png");
```


But you may want to multiple screenshots in your program instead you can write method
in your base test class use it every where. also you may want to put in different directory

```java
public void captureScreenShot(WebDriver driver, String directory, String fileName) throws Exception {
  File scrFile = ((TakesScreenshot) driver).getScreenshotAs(OutputType.FILE);
  FileUtils.copyFile(scrFile, new File("./screenshots/"+directory+"/" + fileName));
}
```

Happy coding.
### sample screenshot by selenium
![sample screenshot](https://www.evernote.com/l/APzrtUX7-FtMkITgNdNhO7nDE9WDM8bib7wB/image.png)
