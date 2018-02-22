---
title: Scrum - A Rant
description: Why I no heart scrum, and you should too!
layout: default
---
<img alt="Unicorn/Scrum" src="{{ "/assets/images/unicorn.jpg" | absolute_url }}"
 style="float: right; padding: 0 0 10px 10px"/> **Developers**
work in a relatively scientific field. As such, it is healthy to have a degree
of skepticism. This is especially true with hype and salespitch. If you buy into
a belief in unicorns, you should be prepared to find a horse with a velcro
horn and a feeling of inferiority to the rhinoceros.

We developers absorb constant messaging about the "latest thing". There's _big
data_, _AI_, _GraphQL_, _SAAS_, _PAAS_, and _AAAS_. It's hard to know which
bandwagons to jump on and which to ignore. The google interview process was once
considered the Holy Grail of hiring practices, and that process has now been
refined. The open office was going to change the world through "collaboration",
and instead, it lead to people posting "WFH - Head down!" on Slack. (That means,
working from home, trying to be productive without interruption!) By and large,
the bad trends get fixed or go away.

So why in the hell is Scrum still around? Is there something redeeming about it?

Having worked on a couple of projects run this way (before I hit the eject
button), I have noticed a couple of things companies might like about Scrum:

1. It's more natural to plan development around two week intervals than to plan
for the long term, during which requirements will change.
1. It's a way to keep junior developers on track, much like an assembly line.
1. It keeps expectations down because it slows development to a crawl.
1. The concept of _stories_ maps well to front-end development, as teams may
have requirements for specific characters using their applications.
1. Scrum is what many people already know.
1. There's a misguided belief that "Agile" is prescriptive process, and "Scrum"
is just a synonym.
1. Truly self-organizing teams are scary.

### What's My Beef?

I've never posted a rant before! I've always wanted my digital history defined
by what I'm _for_ rather than _against_. Recent events have driven me to pile on
to the beef around Scrum. I worked with Scrum for the very first time about
seven or eight years ago, and I approached it with healthy skepticism and an
open mind. When no magic happened, at least when compared to working straight
out of a prioritized issue tracker, I grew a little wary of Scrum.

I watched myself spending hours in "ceremonies" that were focused on process
rather than engineering best practices. I wanted to draw architecture on a
white board rather than putting postie notes in swimlanes. I wanted to argue
the paths to clean code rather than discussing the "definition of done". When I
read an article about a successful team faking past sprints in Jira before the
Agile consultant arrived, both I and the consultant/author became non-believers.
(I would love to find that article again and link to it here!)

Having recently embarked on a job search, I was dismayed at how many companies
are still using Scrum! I made a point of finding out in the first interview
whether a company was using this remedial practice. When they did use Scrum,
I saw a correlation with the size and depth of management. Flatter
organizations with a high proportion of engineers and developers saw little
incentive to adopt Scrum.

### Unicorns Are Fake News

Unicorns are not real, and Scrum does not do any magic. We've heard the claims -- if
Scrum is not working, then you're not really doing Scrum. If you believe that,
I'm going to write a diet plan and sell you the book. If you don't lose weight
on my diet, it's on you!

If it sounds too good to be true, it's not true. I see scrum as _harmful_ because
it requires so much and delivers so little. What's harmful about it? Lots of
things. I'll list them, and I don't care whether any of the things I list are
"true Scrum" or not. This is what people _do_ in the real world, and there are
negative consequences.

1. Draconian sprint scope rules prevent teams from being reactive (aka _agile_).
If you encounter something that needs to be fixed, often that should jump to the
front of the queue. It's demoralizing and inefficient to let bugs fester just to
keep sprints pristine.
1. Scrum ceremonies take excessive time. Ca-ching! That's the sound of wasted
time, and time is money. Developers design systems and write code. Time spent
in "retrospective" meetings, for example, is almost useless. I've never left
a retrospective and thought, "Wow -- that was a good meeting!"

### What's the Alterative?

I said it earlier - I like to define myself by what I'm in favor of rather than
against. The concept of agility is something I can really get behind. There is
an [Agile Manifesto](http://agilemanifesto.org/), but I think the word
_manifesto_ is a bit severe for a philosophy based on flexibility. Agile's most
important statements are:

* _People are more important than processes._ I'm paraphrasing, but this point
implies that processes like Scrum don't build software - developers do. It's up
to us to define and use best practices to ensure quality code and working
software. We don't get working software merely by following Scrum!
* _Working software released frequently._ This is also paraphrased and combines
a couple of points from the Manifesto. The point is that we should build software
in small chunks, constantly checking that the features we've added are working.
To me, this professed value is more of an engineering practice than it is
managerial -- i.e. Scrum. Really advanced teams can deploy new code into production
under advanced CI/CD (Continuous Integration / Continuous Deployment) pipelines.
These pipelines are essentially build, test, deploy, and promote scripts that
bypass the need for human testing. It's a stretch goal for most teams, but
this dramatically illustrates what I think of as working software released frequently.
* _The best architectures, requirements, and designs
emerge from self-organizing teams._ This is a direct quote of an Agile principle
from the Manifesto. Good engineers know what to do and don't require much
oversight. They will build a process appropriate for the team and project, and
they'll constantly adjust team practices for what is and what's not working.

Scrum, by contrast, subjects people to a process and places extreme limits on
self-organization. It puts a time box, usually two weeks long, around
releasing working software. The idea of "showcasing" every two weeks straps
development to an unnatural cadence. If I want to be "agile", I would send the
stakeholders instructions to run my new feature as soon as it gets into my
staging environment. If they want to schedule a meeting, then let's just do
it now so I can move on!

The alternative to Scrum is to build your own practices around the idea that you
will frequently release working software. This is being _agile_, and it does not
require you to do Scrum. There's a mantra for this:

> You can _**be**_ agile, but you can't _**do**_ agile!

### What's Worked For Me?

When teams organize themselves, the tools and techniques they utilize will vary.
There are different types of teams and projects. I've worked mostly on back end
teams in recent times, and here are the team practices that have worked for
those teams.

1. Do daily standups. Some days they just don't happen, so people can just
post their reports in Slack.
1. Constantly groom the backlog. It's OK to do this informally -- meetings
can be hard to schedule, and the backlog can start to drift. 
1. Keep a prioritized backlog based on the needs of teams using your back end
services. Never miss an opportunity to schedule technical debt epics.
1. Define milestones as epics in Jira.
1. Stories are useless to back end teams. Populate your epics with small tasks
in chronological order. Try to keep the tasks under one day's work.
1. Developers pull tasks from the highest priority epic that they are working
on.
1. Create a feature branch off of master for every task you work on.
1. Push the branch to Github and start a code review. When the code review is
accepted by one or more team members, merge it to master.
1. The CI/CD pipeline takes over building, testing, and deploying. This is a
large topic, so I'll leave it there!

Notice how technical these practices are? Using Jira, we still have
transparency with other teams. We're working at a fast clip and deploying
working software (at least to staging systems) many times daily. We focus more
on good engineering than on ceremonies to satisfy the requirements of a
process we did not define, aka Scrum.
