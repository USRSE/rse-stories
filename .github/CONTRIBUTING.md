# Hosting RSE Stories

So you're interested in hosting one or more episodes of RSE Stories? Fantastic!
The podcast is designed so that multiple people, whomever has interest and time,
can contribute episodes. Here is a starting guide for how to do that.

## 1. Engage!

The creator and (current) main host of the podcast is [@vsoch](https://github.com/vsoch),
and you should reach out to her to discuss any questions that you might have.
She is the handle @v on the RSE and US-RSE slack, and can be reached also 
[on Twitter](https://twitter.com/vsoch). Minimally, you should express interest
to her about being a host, and any significant changes you'd like to try.

## 2. Design Your Episodes

You should have a general idea of the kind of episodes that you want to host.
For example, @vsoch takes a minimalist approach and finds people to interview,
and asks open ended questions to prompt telling stories. The content of the episodes
varies, but generally is focused around software, high performance computing,
culture, and spans between industry, academia, and national labs. This might
be your design as well, to:

 1. Engage folks that you want to interview, schedule them
 2. Do some background reading or prepare questions in advance
 3. Record and edit the episode

However, you can also imagine a different idea, for example, to host a specific
number of episodes around a theme. In this case you might:

 1. Decide on your theme
 2. Create a list of people that would be good to interview for it.
 3. Do research and write up a dual story to go along with your interview
 4. Record and edit as you see fit.

For example, you might choose a theme of data storage, do research to write
up (and then record) a brief history, and then add interviews to that. You might
come up with topics of interest, and write entertaining stories to go along.
The format and design of your episode is totally up to you, as long as it
fits in the genre of Research Software Engineering Stories.

## 3. Design Your Branding

The branding of RSE Stories is largely set, but as the host you get to run the
show and introduce the content. For example, you might come up with your
own introductory jingle, and then say something that fits the RSE Stories
(general) introduction style like "`<jingle>` This is Research Software Engineer 
Stories, coming straight at you from `<your-location>`. Each episode
can then open with "Welcome to RSE Stories. I'm `<your-name>` and joining
me today..."

## 4. Find People

Finding people to interview can be tough! Sometimes you are lucky in having
people reach out to you, or connections that are easy to ask to be on the show,
but other times you need to take a leap and reach out to someone that you don't
know very well. If someone doesn't respond, don't take it personally. The
perspective that I like to have is to put myself in the shoes of the average RSE.
I'm likely very busy, and although I might enjoy listening to RSE Stories, 
I don't see myself as being "interesting enough" to be featured on the show.
It's very often the case that our own perspectives about what we do frame us 
as boring because we are used to it, when in fact an outside listener hearing the
story would find much of it novel and interesting. This means that to find people,
it's recommended to:

 - Not be afraid to reach out, either via email or slack
 - Give people freedom to schedule far into the future, or minimally a week in advance
 - Give people a sense of how you will ask them to record, any preparation needed, etc.
 - Always recommend wearing a headset with microphone for sound quality

## 5. Record Your Episode

Recording can vary in how much you invest. @vsoch was able to get a [yeti microphone](https://www.amazon.com/Blue-Yeti-USB-Microphone-Silver/dp/B002VA464S) and use a Zoom account (without video) to record the audio.
The quality isn't as good as you would get in a professional studio, but it's also
cost effective and quarantine friendly to be able to record at home. It's good
to turn off air (or other sound) and record in a smaller space.

## 6. Edit Your Audio

Editing can also be done with a variety of software. @vsoch uses the open
source [audacity](https://www.audacityteam.org/) and starts by applying
a global filter to reduce noise. You likely want to aim for 20 minutes, but
small variance from that is okay.

## 7. Add Your Episode

RSE Stories is released every two weeks, and for the time being you can sync with @vsoch
to see when a release date would work for you. When you have this date, you'll want
to prepare a pull request on your local machine to add it. How does that work?

### Installing Dependencies

Initially (on OS X), you will need to setup [Brew](http://brew.sh/) which is a 
package manager for OS X and [Git](https://git-scm.com/). To install Brew and Git, 
run the following commands:

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install git
```

If you are on Debian/Ubuntu, then you can easily install git with `apt-get`

```bash
apt-get update && apt-get install -y git
```

### Fork the repository

You should obtain a GitHub account and *fork* the <a href="https://github.com/USRSE/rse-stories" target="_blank">rse-stories</a> repository by clicking the *fork* button on the top right of the page. Once forked, you will want to clone the fork of the repo to your computer. Let's say my GitHub username is *meatball*:

```bash
git clone https://github.com/meatball/rse-stories
cd rse-stories/
```

### Install Jekyll

This step is required if you want to render your work locally before committing the changes. 
This is highly recommended to ensure that your changes will render properly and will be accepted.

```bash
brew install ruby
gem install jekyll
gem install bundler
bundle install
```

Then you can can see the site locally by running the server with jekyll:

```bash
bundle exec jekyll serve
```

This will make the site viewable at <a href="http://localhost:4000/rse-stories/" target="_blank">http://localhost:4000/rse-stories/</a>. At this point you can make changes, preview, and open
a pull request when you are ready.

## 8. Open a Pull Request

The episodes are released via a feed that is updated from the [_posts](../_posts)
folder. Thus you should:

 1. Copy a previous post, rename to have the correct date and title for your episode
 2. Make sure that the episode is added under [assets/episodes](../assets/episodes) and named with the episode number and title
 3. Edit the svg file in the [assets/img/coffee](../assets/img/coffee) folder to save a coffee png (titled by the RSE name) for the podcast art
 4. Fill in the markdown for the episode, as described below.


```yaml
---
layout: post
title: "Coming Home"
author: "@vsoch"
rse: "Andrew Turner"
phenotype: andrew-turner.png
excerpt: "Sometimes becoming an RSE is greater than the job description. It's about finding a place where you belong."
date: 2020-05-07 8:30:00
image: andrew-turner.png
media: rse-stories-andrew-turner-episode-17.mp3
length: 14131293
duration: "00:23:59"
explicit: "no"
resources:
 - name: Andrew Turner at EPCC
   url: https://www.epcc.ed.ac.uk/about/staff/dr-andrew-turner
 - name: EPCC on Twitter
   url: https://twitter.com/epcced
---

In this 17th Episode of Research Software Engineer Stories, we interview
Andrew Turner, a research software engineer that leads a team at the University
of Edinburgh, and discuss how research software engineering has brought a sense
of belonging to so many that did not have it before. Andrew shares his hopes
for the future, personal challenges, and a little bit of beauty that you might
not know exists in caving.
```

 - **layout**: can remain post
 - **title**: is the title for the episode. It should be short and sweet.
 - **author** should be your GitHub alias
 - **rse**: the name of the research software engineer you interviewed (if applicable)
 - **phenotype**: is a phenotype image generated at https://rseng.github.io/rse-phenotype and added to assets/img/phenotypes
 - **excerpt**: should be a short excert for the episode - it appears under the title
 - **date**: should be the release date (leave the time to 8:30am is fine)
 - **media**: should be the mp3 file in assets/episodes
 - **length**: if you do `ls -l` for the file, this is the number of bytes.
 - **duration**: the length in minutes:seconds
 - **explicit**: should always be no - if you record explicit content it's not appropriate for RSE Stories.
 - **resoures**: one or more links (each with keys for name and url) that you want to include with the post.


In the bottom (below the header section) you should write any robust text (or extra
markdown content) that you want to include with the post.
When the PR is open, @vsoch will add a CI setup to render a preview automatically. For
now, you can preview locally.
