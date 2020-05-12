---
layout: post
title: "AssertThat in JUnit5"
date: 2020-05-12 15:39:40
tags: [JUnit, JUnit5]
---


In order to use `assertThat()` and `is()` in JUnit5, add Hamcrest library to the classpath and statically import methods.

```java
import static org.hamcrest.CoreMatchers.is;
import static org.hamcrest.MatcherAssert.assertThat;
``` 