---
layout: post
title:  Stale element exception
tags:
- Selenium
- WebDriver
- Java
---
Have you ever seen selenium stale exception in your selenium scripts.
Follow below steps to isolate the error.
This error basically means element you are operating is no longer operatable by
selenium driver.
Follow below steps
 * Start your debugger
 * Isolate the element which is throwing the exception
 * Goto chrome developer tools make sure no ajax requests happened. These things might modify the dom.
 * Check your scripts make sure you page you are operating is not changed. check driver.currentUrl
