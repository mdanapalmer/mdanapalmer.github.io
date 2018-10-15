---
layout: post
title:      "Operator ||= and you"
date:       2018-10-14 23:20:16 -0400
permalink:  operator_and_you
---


Scouring the internet for a definition of an operator can get tedious, especially if you're running into a lot of super technical esoteric mumbo jumbo that beginners (like myself) haven't been able to develop just yet.  Well, friends, I am going to put into words what || = turns into in Ruby.

![What does it mean??](https://i.4pcdn.org/x/1500569380740.gif)

> In Ruby, you can conditionally set a variable like this:
> 
>   x || = 1
> 
> If x is not initialized—or if it is set to nil or false—it will be assigned 1. If it’s already set to a Booleanly true value (i.e., anything other than nil or false), it will remain unchanged.
> 
[Taken from here](http://davidablack.net/dablog.html#2008/3/25/a-short-circuit-edge-case)

In other words:

If x *already exists*, do *nothing*; if x *does not exist*, do *something*.

Our first example is in our School Domain lab in OO Ruby:

[OO School Domain](https://learn.co/tracks/full-stack-web-development-v6/object-oriented-ruby/object-lifecycle/oo-school-domain)
```
def add_student(student_name, grade)
    roster[grade] ||= []
    roster[grade] << student_name
  end
```

Read into human language this means the following:

Add students using their name and grade

**if** roster of this grade **already exists, do nothing; if it doesn't exist, create** a blank array with grade as the value
shovel the student name into the new array that was created if there wasn't an existing array for grade.
end

This is handy to prevent duplication of items.  In the above example, would we want two grade 9s?  

No, of course not!  In a true school only one grade 9 exists.  The same should be in the school domain.   Having two would make our collections incomplete and messy to track.  

I hope this helps anyone currently struggling with the definition of || =.  I kind of want to call it Do OR don't equals.

-Dana


