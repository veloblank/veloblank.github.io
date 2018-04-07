---
layout: post
title:      "Revisiting Old OO Labs"
date:       2018-04-07 09:47:08 +0000
permalink:  revisiting_old_oo_labs
---


I decided to go back over a few OO Ruby lessons, including the labs, to brush up on my raw object orientation programming. I'm finding more forgotten bits of information than I had imagined (or hoped for), so I'm happy to keep going through most of the OO Ruby section to reinforce old learning. I wouldn't say the information is "Aha!" -worthy, but it is important enough for me to highly recommend to any Learn-er to go back over old lessons and labs.

After going through Sinatra and Rails, it's easy to lose how the macros and methods used by the frameworks are built/derived from good old-fashioned Ruby code. A quick "belongs_to" relationship, while easily created in Active Record using the "belongs_to" macro at the start of the class, is also just as quickly made and understood in raw Ruby using the "attr_accessor" macro within a class. For example, the Song class easily "belongs_to" an Artist by:

```
class Artist

  attr_accessor :name
	
	def initialize
	end
	
end


```

```
class Song
  
	attr_accessor :title, :artist
	
	def initialize
	end
	
end
```

The two classes are associated with each other by the Song class having methods (from the attr_accessor macro) that allow assignment of instances of "Artist" to the artist attribute. A Song instance can then expose the name of the artist that is assigned to it through this "belongs_to" association.

To reinforce my learning, I'm forcing myself to redo the labs, including cloning them from Learn again, so that I need to pass the tests and make sure I am checking off everything before I move on. I found that if I just read over my old submissions I don't absorb the information fully. Plus, playing around in IRB and the Learn sandbox and re-typing in my editor is always more good practice. 

I'm far from setting the old weekly goals I had back when I was gung ho web dev in 2017, but going through the labs again is slowly removing my layers of "I'll never get this done" and "Why did I ever start this" onions. Additionally, I've been contacted by some childhood friends that are interested in having an application built for their business. I met with them a few weeks ago to hear what they had in mind and if it was feasible. While it certainly is (and actually could be really cool), I told them about where I am in the curriculum and IRL and how that affects the timeline for the project. They were all understanding and had no issues with MY issues, or even if the project would ever get done, so I really have no pressure to build an amazing, pro-level application until I'm good and ready. 

IRL, I work third shift full-time plus all the overtime my company affords us. This leaves me exhausted nearly every day and my first off-day on Friday nights is spent sleeping in. This has created a pretty skewed work-life balance for almost the last 6 months. I speak with nearly no one, unless it's work-related. My running/cycling/fitness is non-existent but I feel with the better weather coming, I will return to my former glory. I hope the same is true with my web dev'ing.

