---
title: Try/Catch/Finally Expressions in Scala
description: The syntax for defining Try/Catch/Finally expressions in Scala.
date: 2021-06-01
tags:
  - scala
layout: layouts/post.njk
---
`Try/Catch/Finally` expressions are used for catching and handling exceptions in Scala.

Like [`If/Else`](/posts/scala_if_else_expressions), it is an __*expression*__  rather than a __*statement*__, which means that it actually yields a result. This paradigm better aligns with functional programming style.

The syntax mirrors `match` expressions in parts, meaning there are `case` statements inside the `catch` block to match the different possible exceptions.

The `finally` block is optional. Here's an example of a `Try/Catch` expression:

```scala
  val dividedNumber = try {
		10/0 // divide 10 by 0
	} catch {
		// Scala enters this catch block if there's any type of exception
		case e: ArithmeticException => 0 // if it is of the ArithmeticException type, then return 0
		// can enter additional case statements here
	}
```

The `finally` block will always run, whether or not an error is thrown, but it will not return a value. It is optional, and exclusively used for side effects (eg. printing lines to the console).

```scala
  val dividedNumber = try {
		10/0
	} catch {
		case e: ArithmeticException => 0
	} finally {
		println("Hello! This line will always run but is just a side effect :)")
	}
```

Some further things to note:
- Even though `Try/Catch/Finally` is an expression, you are able to just use it as a statement too and ignore the yielded value
- When catching exceptions, you can either return a value to recover (as above), or throw another exception (this exception will not be handled by the `Try/Catch`)