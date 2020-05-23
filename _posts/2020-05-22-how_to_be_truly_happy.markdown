---
layout: post
title:      "How To Be Truly Happy"
date:       2020-05-23 03:02:14 +0000
permalink:  how_to_be_truly_happy
---


Learning to code is not too hard.  Honestly, anyone can code if they put their mind to the task.  Knowing this is humbling.  Even though I feel a rush by creating something that works, I don't believe that I am "God's gift to programming" or that "I know it all" or even "it's my way or the highway".  In other words, I can always learn something new.  My motto is this: ` If I don't learn something new every day, something is wrong`.  What could be wrong?

It could be that I'm thinking too much of myself and I've closed my mind to new ideas.  Or possibly I have stopped challenging myself to learn new things.  Either way, it's not much fun since a stagnant mind is just boring.  We all need to attain new heights in knowledge and understanding.  This certainly makes life worthwhile.

>  If I don't learn something new every day, something is wrong.
> 

I have recently learned some things in Ruby that make my coding life easier and happier.  Look at this example:  

```
def artists
    collection = []
    @songs.each do |song|
      collection << song.artist unless collection.include?(song.artist)
    end
    collection
  end
```

I have used this pattern many times to return a specific part of a collection, in this case song artists.  This works well but is not the best solution.  A more succinct method follows:

```
def artists
  @songs.map {|song| song.artist }.uniq
end
```

The advantage of the latter method is clear just in its brevity.  The ```.map``` method eliminates the need for defining "collection", shoveling into "collection" and then returning "collection" at the end.  Thus, ```.map``` helps keep things nice and [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself).  Yes, ```.map``` returns a new array using the logic provided in the block.  Also, note how  ```.uniq``` limits the return of items to those that are not duplicates.

Here is another example:

```
def self.create(name)
    new_genre = new(name)
    new_genre.save
    new_genre
  end
```

This works well but again can be expressed much more concisely:

```
def self.create(name)
    new(name).tap {|genre| genre.save}
end
```

Here the ```.tap``` method helps by keeping the code neat.  This one line instantiates a new object with the value passed into ```@create```, manipulates the object by calling the save method on the new object, and as a bonus returns this same object.  Pretty awesome!

>   It is more blessed to give than to receive.
>  

I ask myself what would I do without the support of the coding community?  I'm truly grateful for all those that have gone before me and have left so much instruction from which to benefit.  An incredibly wise man once said, "It is more blessed to give than to receive" or translated another way "happy is giving; it beats taking".   I truly believe that, and I hope to pass on any knowledge I gain in the same manner.  

Every day is an adventure in coding; but everyday should be an adventure for everything else too.  By keeping the spark of learning in their mind, anyone can get a triumphant feeling of accomplishment by reaching greater depths of wisdom, whatever their honest endeavor.
