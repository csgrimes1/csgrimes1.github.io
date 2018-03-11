---
layout: default
title: Remote Control - A Home IOT App
description: IOT application running on Raspberry Pi
---
### {{ page.title }}

<style>
    .cols {
        grid-gap: 24px;
        display: grid;
        grid-template-columns: 1fr 2fr 2fr 2fr 1fr;
        margin: 5px 20px 10px 20px;
    }
</style>
<div class="cols">
    <div></div>
    <div><img title="Home" src="/assets/images/remote-control/home.png"/></div>
    <div><img title="Fire" src="/assets/images/remote-control/fire.png"/></div>
    <div><img title="Bravia" src="/assets/images/remote-control/bravia.png"/></div>
    <div></div>
</div>

My Sony Bravia TV is a really nice unit. The picture is beautiful. It runs Android
TV, making it part of a huge ecosystem. There is one issue with the TV that I'm not
happy about: it is really sluggish. The apps seem starved for memory, and the TV
often spends a five count acting on a remote control command.

One night, the TV was in a sluggish mood. I had a thought - maybe the IR system itself
is slow. Perhaps a remote control using my home network would be faster. I downloaded
a Chrome extension that promised to control any smart TV, and it did not work. The
programmer in me thought, "How hard can this be?"

So, I wrote a web service that can talk to my network-enabled things. I have it running
on a Raspberry PI 3. The source code is [here](https://github.com/csgrimes1/remote-control-center).

With any personal project, you learn useful facts and techniques. Honestly, I don't really
use the remote application nearly as much as the actual, physical remote. The best thing
about the project is the number of takeaways I received:

0. You do not need React or any frameworks to write a simple web page application.
0. The `fetch` API is your friend when you need to call a web service. This application
only runs in my house, so I don't care about old browser support. I suppose there's a
polyfill for `fetch` anyway.
0. Font-based icons are easy to use (I used Material Design from a CDN), but there's
a gotcha. If there is an icon you need that is not in the library, it's not easy to find
a solution. In my case, I needed a play/pause icon for my Amazon Fire controller. I solved
it by overlaying two icons, but it took some awkward and brittle CSS to make that happen.
0. CSS grid properties are awesome for table-free layout!
0. Laying out a responsive web page so it displays nicely on a phone requires a bit of
a hack. I had to add a `viewport` element to solve the scaling issues I was having.
0. Docker will not work as you would want on RPi. Why? Raspbian is 32 bit, and your Docker
images will want a 64 bit kernel. Instead, I installed NodeJS on the RPi and `git clone`d
the source code.
0. When you search for '64 bit OS for Raspberry Pi` on the internet, you see the most
unhelpful sort of answers. People respond with, "Why are you trying to do that?" Duh! I
want my 64 bit Linux stuff to work. Hopefully, that niche will be filled in the next couple of
years.
0. You need to use ADB to control Amazon Fire. I supported Fire to keep my web service from
being too tied down to a single TV set.

### Conclusion

As for speed, the remote application is the same as the physical remote. I did not solve
the sluggishness issue! Nevertheless, it is kind of nice to use the application from a browser, where I coded support for keyboard input on arrows, escape, etc.
