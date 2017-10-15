---
layout: post
title:  Introduction to SELENIDE
tags:
- Selenium WebDriver
- Java
---
## Create new java project with gradle in intellij
<p>
    <img src="https://www.evernote.com/l/AAkV1cseKbxKy7x6OBZHKdsGG8HZ7k5tnf0B/image.png" width="100%" alt="Start Project" />
</p>

## Setting libraries

> open build.gradle file


```groovy
dependencies {
    testCompile group: 'junit', name: 'junit', version: '4.12'
    testCompile 'com.codeborne:selenide:4.8'
}
```

<p>
    <img src="https://www.evernote.com/l/AAm3JvR67G1AfL7APL_wz2JzYdqLkpGMNX8B/image.png" width="100%" alt="Start Project" />
</p>


### write your first test
> Create new test files in test directory with below code

```java
package com.specs.login;

import org.junit.BeforeClass;
import org.junit.Test;
import org.openqa.selenium.By;

import static com.codeborne.selenide.Condition.text;
import static com.codeborne.selenide.Selenide.$;
import static com.codeborne.selenide.Selenide.open;

public class LoginTest {

    @Test
    public void gotoLoginPage() throws Exception {
        open("http://qacrm.herokuapp.com");
        $(By.id("authentication_username")).val("heather");
        $(By.id("authentication_password")).val("heather");
        $(By.name("commit")).click();


        $(By.id("welcome_username")).shouldHave(text("Heather"));
    }
}
```
> It should as shown below
<p>
    <img src="https://www.evernote.com/l/AAmL_mUPrRhHrorHsRa7nIiihJTyW7scwSgB/image.png" width="100%" alt="Start Project" />
</p>

### Use chromedriver as browser

> Add below code to build.gradle

```groovy
test {
    systemProperty('selenide.browser', 'chrome');
}
```

<p>
    <img src="https://www.evernote.com/l/AAmD2cMzXytLkqnbypH6IX-u1qf80MDCjDgB/image.png" width="100%" alt="Update gradle" />
</p>

### Let us run tests
>open view intellij menu item select gradle and test task

<p>
    <img src="https://www.evernote.com/l/AAlDLZR7MHVPHodjynvMTYa7sbteN3NSUqkB/image.png" width="100%" alt="Run tests" />
</p>


## Happy testing
