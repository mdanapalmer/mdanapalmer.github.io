---
layout: post
title:      "CLI interrupted"
date:       2018-08-26 04:53:18 +0000
permalink:  cli_interrupted
---


There's a thrill and terror that go hand in hand with boldly going where you've never gone before.  Creating a functioning CLI has been quite the adventure as of yet.  I've been aiming to create a local environment to build this in as it feels intuitively like the right thing to do.  However, I've run into a few snags despite all my efforts.

```
Danas-MacBook-Air:~ mdanapalmer$ ./daily_deals/bin/daily_deals
Traceback (most recent call last):
	2: from ./daily_deals/bin/daily_deals:2:in `<main>'
	1: from /usr/local/Cellar/ruby/2.5.1/lib/ruby/2.5.0/rubygems/core_ext/kernel_require.rb:59:in `require'
/usr/local/Cellar/ruby/2.5.1/lib/ruby/2.5.0/rubygems/core_ext/kernel_require.rb:59:in `require': cannot load such file -- ./lib/daily_deals (LoadError)
Danas-MacBook-Air:~ mdanapalmer$ 
```

I'm not sure why this such file can't be loaded :(  I'm so close.  

All things considered, though, this is a good time for me to go back and review the tough things I wasn't able to fully understand.  I'm a little worried but also excited for my first 1:1 so that I can start moving past this point and get to some actual creation and learning.

yorokshiku onegaishimasu よろしくお願いします
