---
title: If...Else Expressions in Scala
description: How to define and use if expressions in Scala.
date: 2021-05-30
tags:
  - scala
layout: layouts/post.njk
---
In Scala, there are If...Else *__expressions__* rather than If...Else *__statements__*. This means that the If...Else block actually yields a value, rather than just performing actions.

The fact that Scala has if expressions aligns better with the functional style of programming. Using expressions reduces the number of variables that must be declared, making it easier to achieve immutability.

An If...Else expression looks like:

```scala
  val a = 10
  val b = 20

  val z = if (a > b) a else b
  
  // if expression yields 20
  // z: Int = 20
```

It is possible to ignore the returned value, and use If...Else as a statement, however this is not best practice as it encourages side effects and mutation. Example:

```scala
  val a = 10
  val b = 20
  var m = 0

  if (a > b) {
    m = a
  } else {
    m = b
  }
  
  // if expression yields 20, but this is ignored
  // variable m is mutated inside the if...else block
  // m: Int = 20
```
