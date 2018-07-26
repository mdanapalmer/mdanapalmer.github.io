---
layout: post
title:      "Let's Review!"
date:       2018-07-26 03:28:35 +0000
permalink:  lets_review
---

(currently WIP)
As I progress through the curriculum I am finding that I've got a sort of mental block that I'm running into between creating and interpreting code.  This is not unfamiliar territory, as I also encountered this similar obstacle when I was learning Japanese in university.  There are a lot of processes going on and you're asking a lot of your brain.  First, to be able to spontaneously create code, it requires one skill, to be able to read and interpret it is another, and to be able to analyze the errors is another.  So be nice to it and yourself and allow yourself to make mistakes!

I'm going to own my mistakes and make sure that I learn from them.  This lab was a doozy, as the ones before it have been.  So let's get down to business and try to 'parse' the code into human language!


> class Song 

 here, we are defining our class, Song

>  attr_accessor :name, :artist, :genre

attr_accessor is giving us reader and writer methods via macro.  Within this line, there are actually six methods!

>   @@count = 0 

Here is an example of a class variable.  This is going to affect all the instances of the class it is defined within.  The count is set to integer 0.
  
>   @@genres = []

Class variable genres is set to be an empty array

>   @@artists = []

Class variable artists is also set to be an empty array.  
  
>   def initialize(name, artist, genre)
>   
>     @@count += 1
>     
>     @@genres << genre
>     
>     @@artists << artist
>     
>     @name = name
>     
>     @artist = artist
>     
>     @genre = genre
>     
>   end

Now we're cooking with gas!  
The above method is special!  It's a callback, hook, or instance contrustor method called #initialize.  That is, for each instance of Song.new = "Callista" it will automatically generate the properties defined within.

this #initialize method requires three arguments: name, artist, and genre

> def initialize("Callista", "Saki Kaskas", "Electronica")

In addition, we have three class variables we are defining, and three instance variables.

@@count is being set to increment by one each time a new object is instantiated. (indicated by the += operator)


Taking a look at @@genres << genre, we are inserting the genre argument given into the class variable, which is an empty array.  

We are using the #<< (shovel) method to do so. 

Each time the class Song is instantiated, it will insert the genre argument into the @@genres array.  

In this way it can keep track of all the genres that have been given.


Similary, the class variable @@artists is also accepting the argument given for the artist, shoveling it into the empty array that it was defined as.  

In this way, since class variables encapsulate every instance of that class, it keeps track of all of the artist arguments entered.


Now we have some instance variables to define, indicated by the single @ symbol appended to the front of them.  

For each argument, the instance variable should be set to its respective counterpart. (i.e., @name = name)  

This makes the variable input in the argument accessible throughout the instance of this class (and not just to the #initialize method).  

That is its scope, only within the instance itself.

  
>   def self.count
>   
>     @@count
>     
>   end

What is this 'self', you ask?  

Even if you didn't I've got to define it!  

Once you create an instance of this class, how are you going to keep track of it?  

If you don't have a way to keep track, it flies off into oblivion, never to be accessed again!  

So we need to define a method to let us know the count of how many songs have been added to our Song class, but that also knows where to look for that.  

Lucky for us, our instances, or objects, are all self-aware, and the self keyword can reference the class it is defined within.  

Plus, each time we've created a new song, our class variable, @@count, has been incrementing by one!  So calling on it will provide us with this number.  

Congrats!


> def self.artists
> 
>     @@artists.uniq 
>     
>   end

Duplicate artists is a bit silly, since we don't need more than one copy of a song!  The above method references the class again, using the self keyword and checks on the @@artists array.  Notice the .uniq that follows the class variable.  That's a method within Ruby that looks for duplicates, to make sure each entry is 'uniq'ue!
  
>   def self.genres 
>   
>     @@genres.uniq
>     
>   end

Very similarly to avoiding duplicate artists, we also want to do the same to the genre, since it's silly to have two genres that are exactly the same, when we want to be efficient.
  
  def self.artist_count
    artist_count = {}
    @@artists.each do |artist|
      if artist_count[artist]
        artist_count[artist] += 1 
      else
        artist_count[artist] = 1
      end
    end
    artist_count
  end
  
  def self.genre_count
    @@genres.uniq
  end
  
  def self.genre_count
    genre_count = {}
    @@genres.each do |genre|
      if genre_count[genre]
        genre_count[genre] += 1 
      else
        genre_count[genre] = 1
      end
    end
    genre_count
end
end

Also, as a note in reference to the song and artist I am using in this blog: Rest in Peace, Mr. Kaskas.  Your music has touched the lives of so many for the better.  Thank you.
