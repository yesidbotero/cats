---
layout: docs
title:  "Group"
section: "typeclasses"
source: "kernel/src/main/scala/cats/kernel/Group.scala"
scaladoc: "#cats.kernel.Group"
---
# Group

`Group` extends of `Monoid` by providing the `inverse` element of each possible member that fits into `A`.

```tut:book:silent
trait Monoid[A] extends Semigroup[A] {
  def empty: A
}

trait Group[A] extends Monoid[A] {
  def inverse(a: A): A
}
```

Let's see this with an example:

```tut:book
val x = new Group[Int]{
  def inverse(a: Int): Int = -a
}

x.inverse(5)
```
