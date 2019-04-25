---
layout: post
title:      "Let's talk Ruby Method: Return Values "
date:       2019-04-25 00:41:56 +0000
permalink:  lets_talk_ruby_method_return_values
---


It's been just a few months into my journey of programming and I'm trying to walk, talk and think like a programmer - Not always easy but surely fun to experiment. So today, my focus is to break down the meaning behind return values in Ruby 

In the wonderful programming world of Ruby, a method always outputs exactly one definite thing. This thing is called an object. Methods return the value of their last expression evaluated. You can also specify a method's return value with a return statement but with the convenience of Ruby, you don't have to.

Let's take a look at some examples below:

**Explicitly Returning a Value using the `return` keyword:**
```
def add_two(number)
       return number + 2
end

returned_value = add_two(4)
puts returned_value
```

The output should equate to 6 because the value of the last expression evaluated return number (4) + 2 equals 6.

**Implicitly Returning a Value not using the `return` keyword:**

```
def add_three(number)
        sample = number + 3
end
```

The value of add_three(3) is going to result in 6 because the assignment expression evaluates to 6 : sample = (3) +3





