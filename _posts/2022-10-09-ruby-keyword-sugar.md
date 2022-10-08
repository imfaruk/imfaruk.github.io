---
layout: post
title: Ruby Keyword Sugar
categories: [Programming, Ruby]
tags: [Ruby Trick]
date: 2022-10-09 02:50 +0600
---

### Problem
Imagine you have a public gem and it has a `Point` class defined as following

```ruby
class Point
  def initialize(x, y)
    @x = x
    @y = y
  end

  def print
    "x: #{@x} and y: #{y}"
  end
end
```

Its easy to get an instance of `Point` class. You just pass positional argument -  `Point.new(5,7)`

But lest say now you want to provide keyword arguments support. So you rewrite the initialize method.

```ruby
def initialize(x:, y:)
  @x = x
  @y = y
end
```

You have just made a breaking change. All of the users of your gem who have been initializing `Point` with positional argument will now get error.

So how do you solve this problem? All we know is that both

`Point.new(5,7)`
and
`Point.new(x: 5, y: 7)`
should work.

### Solution

```ruby
def initialize(_x=nil, _y=nil, x: _x, y: _y)
  x && y or raise ArgumentError, "Must supply x and y coordinates"
  @x = x
  @y = y
end
```
