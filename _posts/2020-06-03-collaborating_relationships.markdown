---
layout: post
title:      "Collaborating Relationships"
date:       2020-06-03 18:26:57 +0000
permalink:  collaborating_relationships
---


One thing I really like about the Flatiron curriculum is how each new concept or method or thought process is layered on top of what you have just learned, or it’s an extension of what you just covered. There’s always a thread of familiar even if it’s still mostly unfamiliar.

All of the "relationship" labs (Collaborating, Has Many, Has Many Through) were a great example of this layering, extending and feeling sooooooo unfamiliar and awkward for quite awhile. I thought I’d go through some of the basics now, since I’ve finally found myself on more familiar ground (after finishing all the labs, watching ALL the videos and have now started to map out my CLI project — hopefully showing off some of my new collaborating relationship skills, of course).

Object oriented programming allows us to create relationships in order to realistically model the real world.  I have to admit, after having my head buried in these labs for a few ~~days~~ weeks, I was starting to look at the world around me and see relationships everywhere. 

The labs and examples in [Learn.co](http://learn.co) used scenarios including blogs, authors and posts; songs, artists, and genres; and patients, doctors and appointments. I think I’ll take from our dev world and model the relationships among Developers and Clients.

Relationships can be powerful because instead of just referencing a string (very low-level), they allow you access to objects, and all the attributes associated with them. 

In the following example I'm going to show how:

1. Clients **belong to** Developers. (You know what I mean)
2. Developers **have many** clients. (Let’s hope at least one, but more would be ideal.)

### Belongs to.

Each class should know their own name (self) and the name (object) of the other class. 

```jsx
class Developer
  attr_accessor :name
end

class Client
	attr_accessor :name, :developer
end

#create the Developer
sharon = Developer.new
#give her a name:
sharon.name = "Sharon"
sharon.name 
	#=> "Sharon"

#create a client
bob = Client.new
#give him a name:
bob.name = "Bob"
bob.name 
# =>"Bob"

#create the relationship:
**bob.developer = sharon 
	#assigns the developer OBJECT sharon(developer)to the OBJECT bob(client)**
bob.developer.name #"Sharon"
#Bob the client, belongs to Sharon, the developer
```

If we give the Developer class an attr_accessor of :name and give the Client class the attr_accessors :name **and** :developer, we can associate the two.  

As you know, an attr_accessor creates both the reader and writer methods for each attribute.  This allows us to not only set/get the name of a client to itself, we can also set/get the developer's **object** (rather than just a string). 

This is done in the bolded like above: bob.developer  = sharon.  

### Has many.

If you're good at client management (you have to manage all aspects of your growing business!), you are responsible for keeping the list of your clients.  You will need a method that will allow you to access the clients who are owned by you. We can build out the Client class to keep track of all its' new songs with a class variable. 

```jsx
class Client
  attr_accessor :name, :developer

  @@all = []

  def initialize
    @name = name
    @@all << self #each new song will be added to the @@all array at initialization
  end

end
```

In order to access the class variable, we build a class method in Client for the Developer class to use:

```jsx
def self.all
    @@all
  end
```

We can use this instance method in the Developer class, which iterates over the class variable @@all in the Client class, to return only Sharon's (represented by "self") clients:

```jsx
def clients
   Client.all.select {|dev| dev.developer == self}
  end
```

The above returns an array of all of Sharon's client objects, demonstrating that she has many. :) 

```jsx
=> [#<Client:0x0000560bd3e85230 @name="Bob", 
@developer=#<Developer:0x0000560bd3e85398 @name="Sharon">>, 
#<Client:0x0000560bd3e85140 @name="Carol", 
@developer=#<Developer:0x0000560bd3e85398 @name="Sharon">>]
```

Building relationships are rewarding - IRL and in Ruby!  Once I broke through the initial haze of how they work, they are obviously extremely useful and powerful.  I'm really looking forward to writing code with more complex relationships in the future.
