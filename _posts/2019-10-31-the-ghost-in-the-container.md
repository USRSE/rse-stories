---
layout: post-after
title: "The Ghost in the Container"
author: "@vsoch"
rse: "Dockerod Main"
excerpt: "It's good to follow best practices for container building. Otherwise, you might lose yourself."
date: 2019-10-29 8:30:00
media: rse-stories-halloween-2019-3.5.mp3
image: halloween-2019.png
length: 13394787
duration: "00:18:13"
explicit: "no"
---

> This is a special episode of RSE Stories, a Halloween special! All characters and events in this post are fictional. Or are they?

He didn't have a chance to write tests. The deadline for the manuscript was only two days away,
and Dockarod Main had placed reproducibility as an afterthought, an "Oh crap, reviewer three is
going to eat me alive and spit out the little pieces when I don't offer Tensorno
in a container." So he built the container. He shared it on Docker Hub, he had a small
twinge of pain in his chest as it was building in the interface. It looked
so professional, it's Dockerfile proudly displayed, the README from the connected
repository glowing in shades of white and blue. But sometime absence is harder
to sniff out than presence. Sure, you couldn't get security scanning unless you
were in the big players. But what escaped even from our protagonist's awareness
was that there was a process of magic that went on that day, one that would
forever change the course of his life.

The deadline approached, Dockarod didn't sleep - he spent every waking hour
downing fast food, and early released Halloween candy that was typically bought for children
and consumed by adults under stress. It was only early September, but somehow
all the local department stores were ready for Halloween, Thanksgiving, and Christmas.
At the same time. This will be the best "Hallowthanksmas, ever!" he thought sarcastically.
His desk became a wasteland of used fast food
containers, with coffee stain rings creating a new kind of art on his desktop.
His only saving grace was to blame the sticky keyboard on his cat, who frequented
the patio outside to hunt for small rodents and would tromp around on the wet and
sometimes sticky leaves. Why were they even sticky? But I digress. Dockarod was
a shell of a human begin, but like all work remaining magically expands or contracts
to fill the space allowed for it, the manuscript was submit.

The review was eerily quick - it went out for review within a few days, and the 
reviewers returned a positive result within two weeks. Given the impending doom
that Dockarod felt approaching this work, it was a pleasant surprising. But it
was also a bit suspicious. Did they read the entire paper? And test his container?
"Oh well," he thought. It must be that if you add enough buzz words about machine
learning and data intensive workloads the reviewers would become drunken with 
Silicon Valley hype and say "Yes, yes! It's great!" The publication was out
within a week, just before the end of October. It was a blessing and a curse,
because now Dockarod didn't have any excuses to wait around to hear back, he could
continue on with other projects. He decided to return to a previous attempt
to predict scooter stealing based on geographic area. That's useful, right?

The first email came in a few days later. It was from a collaborator at the University
of Vermont that was testing the container. "Great work!" he commented. I can
predict ice cream preferences with reddit posts from the individual about how
they feel about cows. But did you change your container? The paper says that
you used version 4.3.1 of Tensorno, but the container seems to be packaged
with 6.6.6. Is that even a release? Do you think you could take a look?"

Dockarod felt gruffled, which is a combinated of ruffled and gruff. Once a publication
was out, it was very hard to change, and he suspected that perhaps there was just an issue
with the container build. He was going to watch a movie on Netflix, but instead
his evening would (again) need to be used for random work. Dockarod always regret
his life choices when this happened. He didn't want to consider the idea that
he couldn't quell his own anxiety enough to choose to NOT work in the evenings.
He blamed it on his profession, and jumped over to Twitter to complain
about his life choices. Send tweet.

He pulled the container, and the layers cascade into his terminal like a waterfall.
Pulling, extracting, these were all those lovely layers that were generated from
the automated build oh so long ago. Once the manifest and layers were obtained,
Dockarod ran the container with an entrypoint as a bash shell. He was inside!
And now to check the version of Tensorno.

Huh, it seemed to be 4.3.1, he wondered if his collaborator was just downing
a few too many pumpkin ales. But to be completely sure, he ran one of his
analysis scripts against a data file provided in the container.

That's when he saw it. The numbers 6 6 6 were printed in the terminal. And how
were they colored in red? That's kind of... weird. To print colors in a terminal
the terminal would obviously need to support it (his did) but he would need
to print ANSI escape sequences to start and end color blocks. He had done
that a few years ago for a useless Pokemon module, but it definitely
wouldn't have been appropriate to do here. He found this... strange.

But the analysis result seemed to work okay - he used his reddit posts
to predict that he liked chocolate chip cookie dough ice cream. This made him
wonder if he could use a similar method to predict cookie choices, but it would
take rigorous study to know for sure. Anyway, he responded to his colleague.
"You're right, the version is a bit wanky, but otherwise seems okay! Let me 
know if you run into any other issues."

It was later that night when he was helping himself to some rocky road ice cream
(hey, a man can't always be stocked with his favorites) that... it happened.
As he closed the freezer, (pop) there was a shuffle that came from the adjacent cabinet.
He shirked back, knocking over his bowl, "Who's there?" Was it his cat? He opened
the cabinet cautiously, and there was nothing. But then...

> "There's a ghost in the container."

He fell back so quickly that he almost squished his pet cat, who was helping herself
to the fallen ice cream. She sprang up as well, and was gone in the same instant.
What did he just hear? Had HE had too many pumpkin ales to drink? He decided to
skip over his bedtime snack and just go to bed. This was just too much.

He woke up the next morning, and reflected on the dull state of his life. 
Send tweet. But the memory of the voice, that eery, creepy voice, saying something about a ghost in
his container? It stayed with him. With Homer Simpson slipers adorned, coffee in
hand, he set out to take another look. It was just... a container. It was all in
his head. Click click click. Ug, he typed his password incorrectly. Click click click.
Got it! Oh, but ug... two factor authentication. Where was his phone again?
After bypassing the security measures that were most effective at locking himself 
out, he was up and running. He again shelled into the container, and did
a simple listing of the working directory.

Strange, there was a binary sitting right there, named exactly the same as his
analysis script. He must have run this thing the other day when he thought he
was using his Python module! Gosh darn Python paths. Could he blame Python for this?
Eh, probably not. What could he do with this binary thing? Vim wasn't super useful,
it looked like goppelty gook. Even though he ran it yesterday he was super freaked
out and didn't want to do it again. "AH!" he thought, I'll look for it in the build history.

There wasn't evidence of compiling such a binary in his Dockerfile, so he used the Docker Hub
API to request a version 1 image manifest, you know, the older one that still has a v1compatability
key, and then lots of history dumped in there. There was nothing out of the ordinary.
Maybe if he ran the script again, he could trace it this time? Yeah, that would at least
show him in more detail what was going on. It would just predict an ice cream preference after
all, no harm done. Click. And away the binary went.

The TV in the room JOLTED on from nothing with a burst of static electricity
that Dockarod didn't even think was possible for a modern television. It was
the morning news, and they were reporting from a small town on the East Coast.
Dockarod felt his stomach fall to his feet. He felt sick. It was his collaborator,
who died unexpectedly in the night.  His feet went cold. His palms were clammy,
and his face was white. How old was he? Maybe in his 50s? Was it just a terrible chance?
Oh god. He looked back to the trace, and it had finished. And that's when the phone rang.

It was a previous student of his, which wasn't a huge surprise, this student had
called before and liked to talk about her work, ask questions, and probably just
make sure that he was okay. "Hey did you hear about Professor Crane?" I just, I can't
believe it. I think he was really excited about your work... oh god sorry I didn't mean
to make the call really dark, I actually wanted to ask you about the container you shared."

Another issue? What is the deal here? "Sure," he answered calmly, suffocating all
of his internal angst and horror about the recent events. "What's up?"
The student proceeded to tell him that the classifier wasn't reliable - she ran
it a few minutes ago, and then just now, and the first time it gave her
an ice cream flavor of peppermint, and now it was cookie dough.

"Did your reddit data maybe update? If someone else changed the ranking of a post,
well it's a very sensitive algorithm so the result might be different." "Oh," the
student reflected. "That's not very good. I mean, my favorite ice cream is definitely
peppermint. It's kind of disappointing that, I don't know, your classified kinda
got it wrong?"
 
Dockarod silenced a grumble that started to erupt from his ornery crevases. "Sorry
about that, Karina." Maybe you can try downloading the data first, and keeping
time-stamped versions to be sure?

He hung up the phone. He didn't have time for this, the binary sitting in front
of him was emotionally all consuming and he had to understand where it came from.
The trace didn't show much of interest, well, at least he wasn't good enough
with computers to really interpret it. Instead, he sent an email to an old
friend that now worked as a linux admin. They had started on the same path, but
his friend decided that he wanted job security and was fairly terrible at 
data science so he went another route. Yes, Dockarod was bitter, why wouldn't
he be? "Hey Frank, can you take a look at this trace?" I'm like, fairly certain
there is something weird going on. Can you tell why it might change a prediction,
or print out 666?

"Yeah sure," said Frank, who enjoyed relaxing on the weekends, but also didn't
have much of a family and would wind up working on projects. He was a perfect
counter to Dockarod's bias about his own profession being all consuming, but 
again, it was right in front of him so of course he didn't see it. "Hey do you
think you could point me at the container so I could take a look?" Dockarod 
felt ridiculous, but he didn't want to chance it. "Ah, you know maybe if it comes
to that, but I think you can probably get pretty far without it."

He hung up the phone and decided to have some breakfast. On the weekdays was suitable
for forever staining his teeth and tinting his insides with some combination
of nature and added carcinogens, but on the weekends Dockarod liked makin'
waffles. As an extra special treat he liked to add ice cream, so he grabbed
a scoop and dumped it in the mix. It was just minutes later, just as he was
sitting down to a freshly made concoxion with syrup, chocolate chips, whipped
cream and sprinkles, that the voice came to him again.

> "There's a ghost in the container."

He basically crapped his pants. And that's when the phone rang again. It was Frank.

"Hey, so I took a look, and I actually found a string for a URL the binary is requesting,
something about ghost.new, I guess that's a new domain extension that was just released?
But there isn't actually anything there. Everything else seems to be in the container,
so maybe you could take a look at the layers? In the manifest?"

He hadn't thought of that, the history of the container should show the steps
to generate it, but he hadn't double checked the layers. Ug, if only he had done
best practices for layer based images and not put a single command on every run
line. He had a lot of tarballs to dig through. Better have another waffle first.
Yeah and maybe some more coffee.

Three hours of sifting through tarballs, and nothing. He thought harder about the
voice that he kept hearing. Was he becoming schizophrenic? It was totally possible
given his age, and demographic as a white male. But if he didn't hear the voice,
where was it coming from? And what ghost was it talking about?

ps. That's the command you use to list running processes. And there is was, a tiny
little question mark. A ghost or zombie process, if you will. And that was pretty
much all he could figure it. Maybe Frank could help debug this? But this time
Frank didn't answer. He must have finally given in to an afternoon nap or
trip to Target to wander around and buy household items that made you feel good
in the store, but became counter clutter once you were home.

He took a closer look at the binary. Oh wait, he's a total idiot, it was a symbolic link!
Let's just end this once and for all, and delete the thing, and manually push the
container back to Docker Hub. If bad things were to happen every time he ran this 
thing (or was it the ice cream?) the resolution would be to get rid of it.

Rm -rf. And then everything went black.

Dockarod awoke, feeling dizzy and out of place. The surroundings around him were entirely black,
as if someone had sucked out any understanding of light and his eyes hungrily sucked at
the space, hoping for something. Did he even have eyes? Did he have hands?
He followed a small trickle of light and it led him to a flashing marker.
It suddently started to violently change, characters flying across the space
and disappearing into some infinite dark sky. What was up might have been down,
and what was down seemed to always be growing. Oh my god. Was he... no. That's
entirely crazy. Was he inside of... his terminal?

The following sound was overwhelming. He'd never imagined what it might be like
to be inside a computer, it was a world of clicks and hums and constant flowing
of information. When a sound was played through the speaker, or input in the microphone,
it was first passed as data through his space. And somehow, he could hear it.

You see, my dear listener, there indeed was a ghost in that container, but it 
was only a symbolic link - one that was forever connected to its creator.
The link was the only thing preserving Dockarod's existence in what we know
to be the real world, because he died the same night that the container was built,
at the exact instant that it was built, and by some flaw in the universe or space time,
or perhaps because he was so obsessed with his work, his soul became trapped
in the container, and his shell of a real life persisted outside of it.
But now? His connection to the real world is shattered, and he is forever trapped
in the container that turned out to be his final work. 

Welcome back, ghost.


Thanks everyone for listening to this story, it was prompted by a conversation that I 
had with Jacob Chappell on the Singularity Slack, and his original story was
much more succinct:

> It was a Friday at 4:50 PM. My container was almost done building. Then it happened. A kernel update. Security madness. Darkness filled my stomach as I clicked over. "A CVE? Must be serious," I thought whilst munching into an avocado. But then, it turned out to be runc which Singularity doesn't rely on. A rush of relief rinsed over me, and I realized the darkness in my stomach was due to the avocado being old. - Jacob Chappel

and it inspired me to write something fun on my own! The lessons here, if there
are any at all, should be obvious. That we should not be too immersed in our work,
that we should write proper tests for our software, and that we should be very
weary of shared containers, especially when run with a root daemon. Would
the fate of Professor Crane, or our dear Dockarod have been different if there had
been tests? Or execution with different permissions? We may never know.
Dockarod is now the soul of a container, somewhere on Docker Hub,
that even you might stumble upon one day and give a run. We may never know the mystery 
of how life turned to bits, but he's still out there, perhaps an un-named layer,
sitting somewhere without a label on someone's computer, waiting to be brought to life
when someone is interesting in predicting ice cream.

Happy Halloween everyone.
