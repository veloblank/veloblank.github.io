---
layout: post
title:      "Rails Project: Fly Away and be Free!"
date:       2019-07-10 08:37:13 +0000
permalink:  rails_project_fly_away_and_be_free
---


It's halfway into 2019 and this is my first blog post. How can this be? I used to be so excited to write, especially about web development. I liked the idea of researching a topic and forming a coherent thesis and turning it loose into the world. But it was only a matter of time until I got burned out reading other blogs about the web development industry. Mind you, not about student or learning matters, but the obsession about the monetization of blog traffic and the paywalls that came creeping in from Medium (cough cough). This turned every headline into clickbait. I'm a sucker for personal development headlines: "The Power of Waking Up at 4 AM", "Developing a Flexible Mind", "Want to Achieve Your Goals? Prepare for the Messy Middle" all are real, prominent headlines inside of my developer news curator https://www.dailynow.co/ While it is nice to be on the cutting-edge of those types of things, especially as a new developer in an ever-changing industry, it sucked me away from actual work and NEVER let me approach the Deep Work that is so important in the content creation industry.

So, with the ensuing burnout of reading industry-level blog posts, I slowly began slipping away from web development again. I was focusing on working as much as possible at my temp job. It is/was another warehouse job, which, if you like John Oliver, you should watch his latest exposé on warehouses. It will open your eyes to the actual goings-on inside of the warehouses of some of your beloved corporations and clothing brands. After each shift I was physically exhausted. Working 6 days of mandatory 12 hour overnight shifts week after week walking 15 miles each night then begins to sap you. Really the last thing I wanted to do was to sit in front of a computer and learn about web development. It's a terrible thing to have the very "key" to your cage in front of you, and not be motivated to reach out for it each day.

With the encouragement and support of my girlfriend, I slowly started back on the curriculum. I had been sitting at the Rails Portfolio Project for quite some time, but never ready to jump into it. I repeated the labs again and again trying to get the excitement back in me to be sitting in front of the editor hour after hour completing labs, much less creating original, project-grade code.

In the end, it has paid off. My education coach Katie has also been encouraging, enduring the excuses and always remaining positive about things. I shied away from Slack and Study Groups for a long time. My work schedule conflicted with daytime SG's, but in the end it was just my own personal development I had to go through to see the end of this project.

With that, this is my Rails application: Streak on Rails (SoR).

![](https://i.imgur.com/puGZ06y.png)
##The face of the application.

![](https://i.imgur.com/SplguPi.png)
##Login

![](https://i.imgur.com/eBljDwD.png)
##Admin Login gives Edit/Delete privileges as well as a different Nav bar

![](https://i.imgur.com/6xXVNdv.png)
##Admin page for scoring the winners

![](https://i.imgur.com/h8uXWWY.png)
##The Leaderboard with my seed data


![](https://i.imgur.com/lLiHy55.png)
##Shows the users current Streak when signed in

My application models a fantasy sports game by ESPN called Streak for the Cash (SFTC). It has a 'board' of sports propositions each day that you can pick who you think will win the matchup. The matchup is locked once it's started and you must wait for a winner to be scored. If you win, you build a Streak. The highest Streak at the end of the month wins $25,000.

In my application, 'props' belong to a board, and a board has many props. There are 2 types of users in my application, the actual contestants and an admin who must score the propositions as ```winner``` and ```loser```. My many-to-many join table is called user_picks--a user has many picks (or props) and a pick has many users. This join table has 2 attributes that change when a user_pick is ```:scored``` and ```:side_won```. If the user's side won, the Streak is incremented. Otherwise, it returns to ```0```.

Some features of the application are a built-in scraper in the seed file that takes ESPN sports matchups and creates props for the web app.

I really enjoyed building this app. I ran into a lot of new things, like how to create a clickable image 'the Rails way'. *Spoiler:* it's ```<%= link_to image_tag("streak_on_rails.svg"), root_path %>```. The view helpers are combined with the source and path inside of the ERB tag.

I still struggle with having a solid blueprint before building an application. Through my commit history I think I am all over the place with the features and branches. While that keeps me from 'writer's block', it's not a great workflow. I am working on improving that. One thing that helps is practicing drilling in some common design patterns. That means building more and more applications in Rails, but alas, it seems to be more and more a JavaScript world.

With this application I also built out my CSS by hand, like my Sinatra app. While that is satisfying, it can take up a lot of time and leaves a lot of messy HTML and CSS. It feels good to be using a full stack of skills, but I think I could code out a more polished product focusing more on either the front or back end. This application forced me to use a bit of logic in the views (through helper methods), that added classes to the divs so that they could be styled/colored a specific way for each user.

![](https://i.imgur.com/MdLHIKV.png)
Styling wins and losses

A future feature I would like to implement is the use of a scraper to score the props if they are finished. At the moment, the application requires an admin to score a proposition, which frees users who were locked into picks and allows them to pick another prop.

Another feature that creates a board at midnight for the next day would be nice as well. Users may be greeted with this screen after midnight:

![](https://i.imgur.com/uUeKR0G.png)

Here Rails is looking for a board with props. For now the fix is to just run ```rails db:seed``` again.

The repo can be found at: https://github.com/veloblank/silver-chainsaw

As of now I am not hosting it on Heroku. There are some things I want to go over yet between now and my project review. Tomorrow it's the video walkthrough and then on to better things!!
