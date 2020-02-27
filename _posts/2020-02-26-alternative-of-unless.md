---
title: Alternative Of Unless
date: 2020-02-26 07:50:00 +0800
categories: [Programming, Ruby]
tags: [Ruby, Trick]
seo:
  date_modified: 2020-02-27 07:58:42 +0800
---
As a non native english speaker I always find it hard to read statement with `unless`.  I pause for a while to get my head around it everytime I read `unless`. `if !` also feels the same to me. Turns out there is a much more readable alternative.

Did you know that you could write 
```ruby
go_outside if not raining
```
instead of 
```ruby
go_outside unless raining
```
or
```ruby
go_outside if ! raining
```

If you did not then don't be ashamed because I also did not know few days ago even aftr programming with ruby for over 5 years.
