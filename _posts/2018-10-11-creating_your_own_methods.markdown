---
layout: post
title:      "creating your own methods"
date:       2018-10-11 04:24:43 +0000
permalink:  creating_your_own_methods
---


One of the most intimidating things about writing code is the beginning.  When you're staring at a nearly blank screen, cursor blinking, and brain ticking off the ideas you could do.

They're so numerous and yet I find myself hitting a block often.  

Perhaps I'm a bad problem solver (true)
Perhaps I ought to review (I am at the moment)
Perhaps I need a nudge in the right direction that speaks to me in ways that the instructions don't.

Often times it's not a weakness to admit the truth.  I find that most often the truth helps moving forward.

How do we even start?  If we're limited to our toolset to avoid certain methods, how does it work in the background?

Google is my friend, and so is Ben, even though he doesn't know me.  I found his video incredibly helpful, moreso than sitting here scratching my head while I struggled to think of a way to do what needed to be done in the lab.  Learn.instruct is such a great resource, I'm so glad this was shared with me.

https://youtu.be/XRF-CJFZyCg



Let's think about the hints we're given: 

* Think about how to determine which value is the lowest. Do you need to compare each value to something as you iterate?

What's something that can hold a value?  A variable!

* Think about how to collect or store the correct key. Remember that you need your method to return just this key.

What can we use to display the key?  Again, what is something that can hold a value?  A variable!  So versatile.


```
def key_for_min_value(hash)
  low_val = nil
  low_key = nil
	
	# we're using these variables as placeholders for the values of the hash we're going to iterate over.  Then we're going to use those variables to compare against the values yielded to the block.
	
  hash.each do |key, val|
	
	#We iterate!
	
    if low_val == nil || val < low_val
		# here is where we compare, seeking a boolean value.  If the low_value is equal to nil (as it is in our default value) or if the val yielded to the block is less than the low_val is true...
		
    low_val = val
    low_key = key
		#we assign the val and key values yielded to the block to low_val and low_key respectively!
 
 end
end
low_key
#Oh and then we return the value of the KEY!  As instructed.
end

```





