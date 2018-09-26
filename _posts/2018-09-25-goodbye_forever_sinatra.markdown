---
layout: post
title:      "Goodbye Forever, Sinatra"
date:       2018-09-26 03:07:02 +0000
permalink:  goodbye_forever_sinatra
---

It's been awhile since I used the Learn blog dashboard to create a blog post. I've gotten to know more about Markdown and have been pretty independent in Atom, so setting up a new blog post right in the editor is so easy anymore. It's also nice to be able to save it and walk away. I know I know. I'm overcomplicating how easy it would be to just save locally and then cut and paste into the Learn dashboard, but just let me have this one victory.

I am not victory-less, though. I have slain another project. The Sinatra project has been a thorn in my side for an embarrassingly long time. I've gone ahead of the curriculum and dabbled in Rails. I tried to search out easy wins in other modules, just so I could get that red 'Sinatra project unfinished' banner bar off of my screen and enjoy a nice vanquished module. A few weeks ago I left my job; a job that just left me so physically tired each day I couldn't go on with trying to stay up on my Sinatra knowledge, let alone work on this project. 

So I took the leap again, and quit my job. I'm a full-time student once more, who's only distractions now are searching out new vegetarian dishes online and the constant noise of the street by my window. Luckily, I've found the best veggie burger recipes known to man, and I've been trying out https://www.noisli.com. I struggle with Spotify constantly playing music, so a few weeks ago I began playing a lot of ocean waves and peaceful nature "songs" and videos on repeat on Spotify and YouTube. Thankfully, Noisli has a little bit more, including a timer. I'm a big Pomodoro fan so marrying a nice calm end to a pomodoro instead of a bell ringing has been nice. I would suggest Noisli to anyone who is trying to either relax or be productive.

Last week I also got a new keyboard. I decided to go the mechanical route to see what all the fuss was about. I'm not crazy over-the-top about it, but then again I rarely am with things. I like the LED lights on it and the responsiveness. My wireless keyboard was giving me delays and pauses occasionally which made typing very frustrating. This keyboard is wired and works, so I'm happy.

So this has all culminated in me finishing a project. Hooray! It's called Gambol and it is a username/password login CRUD domain that allows users to create lists and add sports bets to the lists for tracking. Sports props can only be created by a user with administrator privileges however, similar to an online sportsbook. Users can see and select any proposition, but they cannot see other users' betting lists.

I also built a route that toggles the user's 'is_admin' attribute:
```ruby
get "/make-admin/:id" do
    @user = User.find_by(id: params["id"])
    if !is_logged_in?(session) || current_user(session) == @user
        redirect "/users/dashboard"
    elsif
      current_user(session).is_admin
      @user.is_admin = !@user.is_admin
      @user.save
      redirect "/users/dashboard"
    else
      redirect "/users/dashboard"
    end
  end
```
The need for refactoring aside, it's a get request from a clickable 'Make Admin' link that first finds the user via the route variable and then checks if this user is the current user. I built this into the route so that someone with administrator privileges cannot accidentally undo their own admin status. On the same line in the conditional statement it also checks if a user is logged in. This prevents anyone from just typing in this URL and changing users' admin status. The redirect to ```ruby "/users/dashboard"``` is quickly redirected to the site's main page if no user is logged in.

Further down:
```ruby
@user.is_admin = !@user.is_admin
@user.save
```
is just the simple switch (and the save) the instance variable needs to toggle from what it currently is, to what it is not (hence, the bang operator). There is a lab similar to this method in Rails, where you must change a student's status from active to inactive.

I could go on about the project. I really enjoyed creating my application, and all the setbacks and subsequent victories made it even sweeter. I feel a tremendous amount of relief now that it's all done, and while I certainly have nothing bad to say about Sinatra, it's just time to move on to bigger and better things.

One thing I did encounter when I was creating the application was an issue with sessions/cookies that I was trying to work through so I could create a persistent sidenav bar that would temporarily hold propositions until the user dumped them onto a list. Instead of just using the prop ID in an array, I was dumping strings into it and I was only able to have 2-3 propositions on the list. Lo and behold: 
![][ruby-error]

Stupid, newbie me. I could just as easily use the prop IDs and place them in the array stored in 'session' and then unload it later when I wanted my list. This would be cleaner coding and definitely the solution to "The Cookie Capacity Caper."

Exhibit A:
![][sidenav]

Well, it's late for me. Off to bed to wake up bright-eyed and bushy-tailed for Rails! It's a new day!
[ruby-error]: https://github.com/veloblank/blog-photos/blob/master/Screenshot%20from%202018-09-23%2018-54-48.png

[sidenav]: https://github.com/veloblank/blog-photos/blob/master/sinatra-blog-post.png

