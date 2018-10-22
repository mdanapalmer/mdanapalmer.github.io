---
layout: post
title:      "Belongs To/Has Many Reciprocal"
date:       2018-10-22 04:45:40 +0000
permalink:  belongs_to_has_many_reciprocal
---


I'd like to help shed some light on this material, as I find having it listed vertically doesn't do much in terms of assisting me in seeing the progress of what we're building up to. 

Let's start with the Belongs To relationship.  The best way to go about being able to do lots of fun things in this case is to think like this:

How do I give this class more functionality?

```
class Song

  attr_accessor :title, :genre

  def initialize(title, genre)
    @title = title
	  @genre = genre
  end

end
```

Right now this Song class is pretty bare.  What can we do with this as it is?

We can create a new instance
```
heleus = Song.new("Heleus", "Soundtrack")

irb(main):008:0> heleus = Song.new("Heleus", "Soundtrack")
=> #<Song:0x00007fb6b7057600 @title="Heleus", @genre="Soundtrack">
```
We can ask the song its title
```
irb(main):009:0> heleus.title
=> "Heleus"
```
We can change the title of the song
```
irb(main):010:0> heleus.title=("Heleus - Andromeda")
=> "Heleus - Andromeda"
irb(main):011:0> heleus.title
=> "Heleus - Andromeda"
irb(main):012:0> 
```
We can also ask its genre!
```
irb(main):009:0> heleus.genre
=> "Soundtrack"
```
And change the genre (or modify in this case)
```
heleus.genre=("Soundtrack - EA")
=> "Soundtrack - EA"
```
This is all fine and good, but it doesn't really give us a lot to work with.  Especially if we want to add an artist to this song.  Sure, we could use a string and build a method, but that's very isolated, and it's not fair to our code to keep it so isolated when it can be stronger with the help of others!

Incoming idea: BELONGS TO

Clearly this song must belong to an artist that made it, right?  That would happen to be John Paesano for Mass Effect Andromeda.

How do we get our song to know that, though?

Let's build a class for Joe

```
class Artist

  attr_accessor :name
	
  def initialize(name)
		 @name = name
		 @songs = []
	end
		
end
```
Cool, done.  We can create an artist instance, give them a name, change and ask for their name, and they're initialized with a blank array to gather their songs in.  Now let's see about connecting Joe to the song he made.

`joe_paesano = Artist.new("Joe Paesano")`

We're also going to change something on our Song class so we can add all of these artist things to it

ORIGINAL:
```
class Song

  attr_accessor :title, :genre

  def initialize(title, genre)
    @title = title
	  @genre = genre
  end

end
```

NEW AND IMPROVED:
```
class Song

  attr_accessor :title, :genre, :artist

  def initialize(title, genre)
    @title = title
	  @genre = genre
  end

end
```
Check out that artist attr_accessor!  Now we can write methods that contain that information in them!

heleus.artist = joe_paesano

heleus.artist

```
heleus = Song.new("Heleus", "Soundtrack")
=> #<Song:0x00007fb6b694b410 @title="Heleus", @genre="Soundtrack">
irb(main):043:0> heleus.artist= joe_paesano
=> #<Artist:0x00007fb6b889fc58 @name="Joe Paesano">
irb(main):044:0> heleus.artist
=> #<Artist:0x00007fb6b889fc58 @name="Joe Paesano">
```

Check that out!

We connected the Artist class (and our joe_paesano instance) to the Song class (and the heleus instance) together without breaking a sweat!  All because of some very cool attr_accessor capabilities.

Coming up?  The Has Many relationship (There's a little hint of it in here, if you're eagle-eyed, you may notice it!)


