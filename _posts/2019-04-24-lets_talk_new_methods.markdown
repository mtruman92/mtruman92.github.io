---
layout: post
title:      "Let's talk .new methods"
date:       2019-04-25 00:37:56 +0000
permalink:  lets_talk_new_methods
---


The goal is that by the end of this blog, .new is clear and consise. This is especially important in Ruby when we're working with classes. So let's break it down.

### **Classes**
I like to think of classes as categories. So I can have classes of different categories like dogs, cats, horses, turtles and so forth. And for each of these categories (classes) we will make an object. The class describes what that object knows about itself and what that objects functionality is.

###### Dogs (this will be our class)
* what it knows :  name; :breed               -----> instance variables
													 
* what it does    :talk										                 -----> instance methods

**Instance Variables**: In this example above, the dogs know their name and their breed (things an object knows about itself)

**Instance Methods**: In this example above, the dogs serve purposes such as talking (barking) (things an object does).

We use the class keyword to start a new class definition:

```
class Dogs 

> def talk
>      puts "Bark!"    
> end		 

```

**class**: declares a new class 
**Dogs**: class name
  
```
**Instance Method**  
 > def talk   
 >    puts "Bark!"    
 > end		     
        
```

**end**: end of class declaration

# Creating New Instances (Objects)
If we decide to call the new method on the Dog class, it will return a new instance of the Dog class. At that point, we can designate that instance of the Dog class to a variable. For example:

```
> max = Dog.new

> chips = Dog.new
> 
```
Once these instances are created, we are able to call their instance methods. For example:

`max.talk`

With the classes defined, we can create new instances of those classes -> New objects 
Now both of our dogs can bark if we wanted them too and we can also create new dogs to add to our collection :)


