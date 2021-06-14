---
title: Defining a function in Scala
description: The syntax for defining a function in Scala.
date: 2021-05-27
tags:
  - scala
layout: layouts/post.njk
---
Scala has both functions and methods. A Scala function is a standalone object, whereas a method is essentially a function that is defined as a member of a class.

The syntax of a function (in pseudo-code) looks like:

```scala
    def functionName ([params]): [return type] = {
        // body of function
        return [expr]
    }
```

A function in action looks like:

```scala
    // one-liner
    def add (a: Int, b: Int): Int = a + b

    // multi-line function
    def add (a: Int, b: Int): Int = {
        var sum: Int = 0

        sum = a + b

        return sum
    }
```

Some further things to note:
- Scala can infer the parameters of a function, but not the return type
- Scala permits functions to be defined within functions
