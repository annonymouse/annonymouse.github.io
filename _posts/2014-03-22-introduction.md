---
layout: post
title: "Dissertation() = blog -> Dissertation() [] done -> STOP"
description: "why am I here?"
category:
tags: [oxford, aboutme, dissertation, csp, concurrency]
---
{% include JB/setup %}

So I'm a full time employee at a large software company and also a part-time
student of the [Oxford Software Engineering
programme](http://www.cs.ox.ac.uk/softeng/).  As part of that degree I have to
write a dissertation on a topic of my choosing, somehow related to the field of
software engineering.  As I want to break up the writing of this dissertation I
thought I'd start blogging about things as I figured them out and hopefully make
this blog a rough first draft of my dissertation.  This has worked out for other
coursemates of mine so hopefully I follow in their footsteps.

Or at least, that's the plan.  It is also possible that this is the last post
ever.

I'm currently interested in concurrency frameworks and libraries, and the plan
is to look at a few of them an try to apply them. Hopefully I'll learn something
along the way (which is pretty much all I want in life).  This is what I've
submitted as a proposal.

However after having recently done a course in model checking using machine CSP
it's peaked my interest in it's possible applications for my dissertation. I
could probably model one or two of the examples I hoped to rewrite as part of my
testing... but I'm worried about biting off more than I can chew here.  Given
that my title for this page doesn't really accurately model progress through the
dissertation probably says something about my ability here.  Maybe it should
look more like this

    Dissertation(p) = blog -> Dissertation(p+1)
                    |~|
                    (p > ENOUGH_WORK) & done -> STOP

Note here that even when I've done enough work I may not be done.  And really, I
should be able to do less work.

    Dissertation(p) = (blog -> Dissertation(p+1)
                    []
                    procrastinate -> Dissertation(p)
                    []
                    change_idea -> Dissertation(0))
                    |~|
                    (p > ENOUGH_WORK) & done -> STOP

Maybe the above is more realistic, but the statespace is massive probably
because of passing p.  I really should study more...

Anyway that's all folks.  I'll be writing more as I go on but first I need to
finish my model checking assignment... so we'll see how that goes.

