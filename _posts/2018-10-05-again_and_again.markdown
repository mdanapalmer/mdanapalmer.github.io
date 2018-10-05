---
layout: post
title:      "Again and Again"
date:       2018-10-05 05:34:19 +0000
permalink:  again_and_again
---


I find myself back where I started, with more perspective.  In an effort to try and keep up with a curriculum, I find I've lost my way.  Back to variables with me, it is.  In a way this is a positive, as I'll have a second chance to look through the material.  But on the other hand, I can't discount the negative, since it needs to be acknowledged.

I'm disappointed in myself for my lack of comprehension, for my lack of genuine progress.  My heart is still in this, but the shiny-eyed wonder and amazement have faded.  Effort only brings you so far, and I desperately hope I'm not making a mistake.

So I'll carry on doing what I can in the hopes that eventually... eventually it will click and make sense.

With that out of the way, let's set some realistic goals.  Working full time and tending to all the needs of a household on my own really isn't something I can dawdle with.  My job isn't where I want to be as a career.  This is my chance to escape that and make something of myself.

If I can help anyone, I hope to be an inspiration, not an example.

Let's review what we've got so far.

Variables; they're what you use.

I like to think of variables like jars, and the value of the variable what you put inside that jar.  The value is protected by that jar.  But you can unscrew the jar and put in a new variable as well.

There are also things that we can do to the jar that make us see the value inside the jar differently.  We can shine light in it, we can magnify it, we can change the color of the glass.  We can liken this to calling methods on our variable, but at the core the value won't change unless we unscrew the jar and put a new item/value in it.

Take the example of the variable sound = "squeak"

If we call .upcase on sound, what's returned is "SQUEAK" 

sound.upcase #=> "SQUEAK"

you could say we've added a colored light into the jar that changes the appearance of the value inside that jar.  But has the value inside that jar actually changed?

To confirm, we can call sound once more.

sound #=> "squeak"

Unless we actually change the item/value inside the jar by explicitly doing so, the jar will still contain the original item/value.

I'll add some images to this later to help illustrate what I mean.  Essentially, this is what is called "pass by value".  

Another example is the following

> a = 1
> 
> b = a
> 
> a = 2
> 
> b = ??
> 
> b = 1


