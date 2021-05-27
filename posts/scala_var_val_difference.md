---
title: Difference between var and val in Scala
description: Discussing the difference between var and val in Scala, and how you should use them.
date: 2021-05-27
tags:
  - scala
layout: layouts/post.njk
---
`var` and `val` can both be used to define values in Scala, but differ when it comes to mutability. Generally `val` is preferred, as it better aligns with the functional programming style.

## var

`var` represents a variable. It is a mutable reference to a value, meaning its value can change. Similar to `var` or `let` in JavaScript.

```scala
  var x = 123 // defines variable x, of type Int

  x = 321 // x can be redefined to 321, since it's a var
  x = "hello" // x cannot be redefined to a string, since x is of type Int
```

## val

`val` represents a value. It is immutable, meaning its value never changes. Similar to `const` in JavaScript.

```scala
  val x = 123 // defines value x, of type Int

  x = 321 // x cannot be redefined to 321, since it's a val
```