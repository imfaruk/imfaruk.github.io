---
layout: post
title: Alternate way of writing 'unless' statement in Ruby
categories: [Programming, Ruby]
tags: [Ruby Trick]
date: 2022-09-05 03:41 +0600
---

As a non native english speaker I always find it difficult to read statements with `unless`. Whenever I see `unless`, I pause for a few seconds to get my head around it.


Actually the word `unless` is equivalent to `if not`. So saying `Go out unless raining` is same as `Go out if not raining`.
`unless` syntax is something that other traditional language does not have. They use `!`. In ruby we can use both. It even allows us to use `if not`.

All three statements are equivalent:

```ruby
go_outside unless raining
go_outside if !raining
go_outside if not raining
```

To me the third one is much more readable compared to the first and the second.

