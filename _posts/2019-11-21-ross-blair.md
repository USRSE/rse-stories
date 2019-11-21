---
layout: post-after
title: "The Lab Without A Couch"
author: "@vsoch"
rse: "Ross Blair"
phenotype: "rwblair-rse-phenotype.png"
excerpt: "Ross thought he might want snacks and nap-pods, but found happiness in The Lab Without A Couch"
date: 2019-11-01 8:30:00
media: rse-stories-ross-blair-episode-5.mp3
image: ross-blair.png
length: 10172081
duration: "00:13:51"
explicit: "no"
resources:
 - name: Ross Blair
   url: http://reproducibility.stanford.edu/team/ross-blair/
 - name: The Lab Without A Couch
   url: https://poldracklab.stanford.edu
---

This week on RSE stories, we're going to give you a little bit different kind of episode.
We're introducing a new interview format that is text based, meaning that the engineer
being interviewed answers questions over email, and then (being true to the name of
this podcast) we write and record a story. Why are we doing this? It removes selection
bias that would hugely prefer extroverted folks. You know, not everyone wants to be
recorded as they are speaking.

For this inagural episode, we tell the story of Ross, a research software engineer
at Stanford. But actually, I'll stop there. You can read Ross' answers to my questions,
or listen to the story directly to learn more.

## Interview with Ross

> So you're a software developer in a lab at Stanford, and you work on
> quite a lot of tools! Could you tell us a little about your position, and some of your
> story for how you wound up at Stanford?

I graduated from The Evergreen State College in 2011 focusing on CS. While there I worked as a system administrator for the various on campus computer labs. After graduation I worked for a webhosting company as a Linux System Administrator for a couple years. After that I transitioned into being a contractor working mainly in Python but dealing with any language necessary (C# and PHP are now just bad dreams I once had). I worked on projects for irrigation districts in West Texas and did work for a small software company in Seattle. I ended up in Palo Alto because my SO was getting their PHD, once my contracting work dried up I started looking for a local job. I found a job posting looking for help making a Django site to host freely accessible fMRI datasets and it sounded like something I could do.

> Do you consider yourself a research software engineer, and had you heard this
> term in the past?

It's not a term I hear used a lot but it makes intuitive sense. Personally I shy away from the 'engineer' title, there's a certain amount of rigor to what say a nuclear or civil engineer does that doesn't seem present in what I do, but the E word has been creeping into the tech employment vernacular so I guess there's little I can do to stop it.

> Tell us about the scope of tools that you develop.

I was originally brought on to make openfmri.org but this has been supplanted by openneuro.org which isn't developed by me. From there I went on to  help maintain a lot of different projects mostly websites, here's a run down of the projects I deal with on a regular basis:
Cognitive Atlas - "a collaborative knowledge building project that aims to develop a knowledge base (or ontology) that characterizes the state of current thought in cognitive science"
Expfactory.org - a site out lab uses to deploy experiments to mechanical turk and record results.
NeuroVault.org - "A place where researchers can publicly store and share unthresholded statistical maps, parcellations, and atlases produced by MRI and PET studies."
NeuroScout,org - "A platform for fast and flexible re-analysis of (naturalistic) fMRI studies"
bids-validator - The BIDS standard made manifest, it tells people if their files are organized properly.

I also sometimes help out with the *MRIPrep family of repositories that are used to pre-process a variety of imaging data, lately just working on their automatic document generation tooling.

I also find myself in charge of our labs AWS account so any type of administration with that I do, I probably spend less than an hour a week doing that type of admin work.


> (Remembering that you came from industry) can you share with us what it was like
> to work in industry, and what led you to look into academic positions? (Or why did
> you start looking for a RSE position - did you know you might like research?)

I found industry pretty miserable, most places I worked there was always an intense focus on deadlines whether it was for a good reason or not. The other thing about it was not being able to take pride in the products being worked on, things that existed to make money not necessarily any ones life better.

I didn't set out explicitly looking for an RSE position, but I came across a job posting for one that aligned exactly with my skill set at the time. I had no idea what it would be like, but the requirements were clear and after the people I met through interviewing seemed reasonable so I didn't hesitate to take it. Now I'll never go back to private industry if I can help it.

> When you were looking, did you know the kind of role you were looking for?
> How hard was it to find roles to build research software?

The job I got was the only RSE position I applied for, but there were a few others I had eyes on if this didn't work out. There were dozens of relevant listings at Stanford at the time, I don't know how quickly they filled. The compensation levels for most RSE jobs I know of are not competitive with private industry so they seem to take longer to fill. As to what I was looking for, it really was just something that aligned with my skills at the time.

> How involved are you with the daily operations of the lab (everything from lab
> meetings to get togethers to writing papers?)

I recently became remote full time so I am much less involved in the day to day operations at the lab by virtue of not being there. I still find myself in about 2 to 3 hours of meetings a week with people in the lab which goes a long ways towards not feeling completely in the wilderness. The lab currently has two other full time RSEs that are remote, which is a testament to the housing and cost issues of the Bay Area.

> What is the hardest part about being an RSE?
Keeping up to date on the newest libraries or tooling. I find I don't spend very much time on learning new things unless they are necessary for the problem at hand. I can imagine if I ever try and find another job in a few years I'll have a bit of catching up to do.

> What is the best part about being an RSE?
The freedom and lack of pressure. I'm trusted to do what's expected of me and most of the time there is not an immediate deadline causing rushed work. I mentioned compensation earlier, and freedom in work and from stress are worth more to me than a larger pay check.

> What is something that you do in your role that most folks wouldn't expect?
I wish there was something exciting I could say here but its really just a lot of fixing bugs. Our lab is good about acknowledging people who make their work possible so my name has ended up on a few papers which I find very flattering. Also got to get an MRI scan prototyping an experiment once which was is not something I had ever done before.

> Do you work with a team, or primarily on your own?
For solving individual problems I'm usually working on my own, but every project we have has people around it that make it possible so in that sense my work is always in support of a team.

> How do you set your goals, both personal and work related?
I don't! I really thrive in a role where people other people are coming up with the goals and telling me what they'd like to see done. As for personal goals, I'm sure I have them but I don't actively see them as such. I don't like to compare myself against benchmarks or put pressure on myself to be something I'm not, so my personal development seems to be optimized towards producing as little stress for myself as possible.

> What kind of resources (training, software, compute, or other) or community
> could Stanford offer that would make your life better?

I'd love dedicated hardware for webhosting so we didn't have to use third party services for simple stuff. I have a headless tower in my office on campus that I use for a variety of tasks, serving some files, running tests, etc. Its silly that I should have to be in charge of that hardware and the only place for it to live is in my office. I've never really done formal training, the listings for Stanfords professionalization classes just aren't relevant to my skill sets so I ignore them.

> What's the weirdest thing about Stanford or the Bay Area to get used to?

I lived in Palo Alto for about 6 years and I never got used to it. Everyone had so much money and so much of everything. There were a lot of entitled residentialists that complained about every thing. Most of it didn't feel like reality. I have trouble putting it into words. One thing that got me was complaining about there being too many jobs in the area, its like 2008 never happened to a lot of people in this part of the world.

> The answer is machine learning - what's the question? (This one is supposed to be fun/
> creative, take it anywhere you like lol)
What is overrated for $200. The advances in the past 5 years have been amazing, and the tooling around them is continually improving but I think the investors of the world have oversold the number of problems it will solve and how well they will solve them in terms of day to day living for normal people.


<img src="{{ site.baseurl }}/assets/img/posts/lab-couch.JPG">
<small>The lab didn't have a couch, but there were ways around that.</small>
