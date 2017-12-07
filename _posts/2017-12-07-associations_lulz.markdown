---
layout: post
title:      "Associations: Lulz"
date:       2017-12-07 15:42:34 +0000
permalink:  associations_lulz
---

A painful reminder about *understanding* a concept came in the form of associations between models and their data. I've struggled with this since I first saw the words *belongs_to* and *has_many*. The concepts seem fine as I read through the Readme, but every time I go to the labs, I find some way to just blank on properly associating the models.

The *subordination* of a model to another can help, as a post *belongs_to* an author and an author *has_many* posts seems intuitive. In real life, this is just how it is--the post just *feels* subordinate to a human author. But what about in an app, where there are seemingly infinite ways to associate data and models? How is a developer to know if a ride belongs to a passenger or to a driver or to a taxi? Which model *has_many* and which model *belongs_to*? Which model is subordinate??!! 

These are my current Rails struggles. While it's quite easy to write passing code because of the tests and their outright descriptions for *why* it failed, I feel like I sometimes need a reminder that writing code that's not test-driven can be quite subjective (and thus fun). My associations matter based on what I want my app to achieve as an end-product. If I were designing a ride-sharing app I might make different associations to generate different data, but until then, I have to satisfy the unit tests.

I've got foreign keys burning a hole in my pocket! I need to find tables to put them into!
