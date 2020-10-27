---
layout: post
title:      "Sinatra Project - ClassTech"
date:       2020-10-27 10:02:45 -0400
permalink:  sinatra_project_-_classtech
---


Below are a few ramblings from my Sinatra project build. It was such a great learning experience and I can't wait to show it to my friends. Read on...

## Solve your own problem

As a software engineering student, we have the task of choosing what we make for our projects, with very few restrictions, as long as the requirements are met. I've definitely been frustrated with this job, as it can be daunting to find the Goldilocks ("just right") project.  Not too ambitious, not ambitious enough, not too boring, not too complicated...you know what I mean. You've been there.

On the other hand, it's quite a little luxury. 

I feel like I hit the jackpot when my project idea came from something I needed. It solved a very real problem for me and fit perfectly into the requirements.  As we learned about classes and objects and how to make them work together (magic!) throughout the curriculum, I started to think about things in my life that way. The idea wasn't far behind. 

When my daughter was in 3rd grade, she was convinced that every girl in her class had a phone. They would talk about chats they had late in the night and all the virtual socializing they were doing outside of school. Naturally, my daughter felt left out (as her father and I have decided to 'wait until 8th' grade for a phone for her - at the EARLIEST). Now, I knew these girls didn't have the tech or access to it the way they described since their mother's are some of my closest friends, but my daughter wouldn't believe me. 

So I created ClassTech. It's an app that would be used by each parent in a child's class, to show others in the grade what tech their child has and uses. A golden source, if you will. Check it out <a href="https://github.com/sparsell/classtech">here</a>.  (Someday, I would love to actually release it!)

The fact that this app is something I needed made me all the more passionate to build it. And through this success, I have more ideas for my next three projects brewing away, ready to take off once I hit Rails, JS and React. My whiteboard is already a mess...

## Build as you go

Being a self-paced student, and having my shiny new software engineering study schedule completely thrown out the window by the coronavirus craziness only two weeks after I started, I decided on a parallel approach to learning Sinatra while building at the same time.  Having my project idea before I started gave me a very real way to think about the new concepts I was learning. I could try things out with my own models and it really helped to solidify what I needed to build. 

Sure, I ended up starting over a few times but that in itself was great practice. A lot of what we are learning isn't complicated, it's just unfamiliar. (A fellow student wrote that, and I'm sorry I can't remember which blog it was so I can't give proper credit.) Repetition makes the unfamiliar familiar. And that gives us confidence that we have *almost* nailed it. 

## Don't be afraid of challenges

About a week before I was about to declare my project finished, I realized I had set up an association  wrong. (Yes, even with all that practice!) My app wouldn't do the ONE thing I really wanted it to do!  I needed a join table to represent the fact that Children have many Devices and Devices have many Children. (I had set it up as a belongs_to association so you couldn't see how many kids had an iPad or a Chromebook - there was only one of each!)

I'm sure I had been coached to do it correctly (with a join table), but at the time I was still crawling and was likely focused on other areas, so missed the great advice. It really wasn't the end of the world. I laughed at myself and honestly, felt a little proud that I figured out what was wrong on my own. You have to celebrate the small stuff, right? (More on that below.)

Over the weekend, I took notes on all the steps to change my association and by Monday afternoon, it was done. And it worked. 

## Use the resources

Just because we don't have the ability to use AAQ for our projects, doesn't mean we are on our own. 

1. Study groups (a million thanks to Dustin and Dwayne!): I mean, they are awesome. 
2. Flatiron videos of Sinatra builds: 
    - I loved Ayana's complete build series, starting with <a href="https://www.youtube.com/watch?v=ce7yZGWTrOk&feature=emb_err_woyt">this one</a>, and
    - Jenn's route protection <a href="https://instruction.learn.co/student/video_lectures#/343">video</a> was also extremely helpful.

        Me: Watch, pause the video, think it through, test it out in my code, rewind, watch again. Repeat. 

3. Sinatra Slack channel: find others in the same place as you, a second pair of eyes to review your code, or get someone to help you debug. 

There's just no reason to go through it alone. It can be frustrating, demoralizing and make you think all kinds of crazy thoughts about not having learned anything. That's not what we are here for and quite simply, it's just not true. 

## Celebrate

I am ridiculously proud of how my project turned out.  I learned so much, held myself to my own schedule, stretched myself to do more, and really strengthened my ties to the learning community. 

My daughter LOVED the app when I showed her and I'm super excited to show my friends - my biggest fans in all of this. (Because, we all have kids who want phones and think they are the only ones without!)

Now, on to Rails...
