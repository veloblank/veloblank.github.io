---
layout: post
title:      "Submitting CLI Gem (Finally)"
date:       2017-09-10 12:04:11 -0400
permalink:  submitting_cli_gem_finally
---

It had to be done. I couldn't look at that crazy, red "project overdue" banner anymore. I finally submitted my CLI project. It's been a crazy ride. From abject fear about how to start, to writing terrible opening code, and trying to re-learn concepts and how to set up my environment files so everything could 'talk' to each other, to overhauling lots of code again, I had to just sit down and grind this out. While it won't win any awards, it is something that I'm extremely proud of creating. I didn't stray far from my original concept, but I didn't see the process shaking out like it did.

For starters, I took about 6 weeks off in the summer from the program. I was trying to code and work my hours and do too much at the same time, and it was affecting the quality of my learning and the quality of my life. Over that time I regret staying almost completely away from coding and totally away from my project. When I started up the program again I was completely lost about simple Ruby and programming concepts and had next to idea where I was going in the CLI project or what my code was doing. I regret that in hindsight, much like I regret a lot of how this year has gone so far for me, in hindsight. But I've committed to righting the ship and I've found already how much that has made me a better person. ![](https://az616578.vo.msecnd.net/files/responsive/embedded/any/desktop/2016/12/05/636165776261245895-646855178_i1.wp.combitcast-a-sm.bitgravity.comslashfilmwpwp-contentimagesmoana-boat-sailing-wave-700x398-d5d924f01018c3d1f6a4540b8025fb9cfa7392e7.jpg)
The concept for my project was to scrape a fantasy sport site from ESPN that would allow a user to read the sports 'props' for the day and read more about them. The CLI presentation of this was pretty straight-forward, text-based styling, but I did get to use the 'colorize' gem to present things a little more stylistically. This has given me an appreciation for CSS. This is a look at the CLI:

![](https://i.imgur.com/wyPISPr.png)

The user chooses which prop they want to read more about. As an additional feature, I made it possible for the user to make a selection, using the user's default browser. This is somewhat of a gray area because automating picks and botting are against the site's TOS, but the app user is still making the picks in real-time, similar to a phone app. Future features could be implemented where picks are persisted in a database and then launched at a preset time so a user could make, say, 10 picks in a day without even being around a phone or computer. This is clearly against the TOS of ESPN, and since I enjoy playing the game as-is, I haven't really decided yet how far I will pursue these features besides the educational nature of it, but I don't think I will be releasing this as a gem because of it.

My code was pretty clunky at the outset. I'm amazed by how much I learned just by sitting for HOURS and HOURS and HOURS debugging with pry, reading on stack overflow and just thinking about what I wanted my code to do and how I wanted it to do it.

Rest assured, this project is not over after my assessment. I realized the importance of having on-going side projects, not just in school, but in my future as a developer. It keeps you sane, even when real life is insane around you, and projects at work are boring. I hope to expand on this project by starting to add SQL and some other database code into it, as well as refactoring to make the code sleeker.

Good luck to others who are going through the same thing now!
