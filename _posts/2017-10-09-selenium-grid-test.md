---
layout: post
title:  Selenium GRID on cloud
tags:
- Selenium GRID
- WebDriver
---
If you want to test your tests on selenium grid. I deployed one on google container use it as shown in below example.
```java
driver = new RemoteWebDriver(new URL("http://35.193.227.180:4444/wd/hub"), DesiredCapabilities.chrome());
```
