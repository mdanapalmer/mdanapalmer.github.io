---
layout: post
title:      "Progress in spite of frustration"
date:       2018-09-27 05:15:54 +0000
permalink:  progress_in_spite_of_frustration
---


Every bit is a hard fought battle.  But every bit is worth it.  Today I finally managed to learn about the difference between referencing a variable and the value of it.  Ruby, being a pass by value language, keeps track of the value of the variable.  In other words.

a = 1
b = a
b = 1

Now we need to consider the value of a being 1.  setting b = to a we find the value of b is also equal to 1.

But what if we reassign a?

from the beginning:

a = 1
b = a
b = 1
a = 2
b = ?

has the value of b been reassigned?

Should you input the following code into repl.it or your own terminal you'll see that b retains the value of 1.  b is not reassigned because a has been, b continues to hold onto the value of a even if a itself has been reassigned.  

I think this would be best illustrated with images, and I found a website which provides as such, though it's a dense read: https://launchschool.com/blog/references-and-mutability-in-ruby

I hope this helps!
