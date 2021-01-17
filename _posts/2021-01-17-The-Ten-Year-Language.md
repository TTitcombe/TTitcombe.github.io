---
layout: post
title: "The Ten-Year Language"
---
I recently read the Paul Graham essay
["The Hundred-Year Language"][hundred-year],
in which he envisions what the programming languages of the future
will look like.
While it makes for an interesting intellectual exercise,
most people reading it won't have use
for the language of the next century.
Far more interesting
is the language of the next decade.
So, what is it?

_Note that in this piece
I use "hack" in the same context as Paul:
piecing together software;
"quick-and-dirty" development;
creatively solving computational problems.
I do not mean somebody trying
to illicitly gain access to another system._

Before looking forward to the latter stages of the 2020s,
we first must look back over how things have changed since 2010.
The clear champion of this decade is Python:
Python is popular among beginners
because of its readable syntax,
but it has grown even among experienced programmers because it is,
more than anything else,
hackable.
You don't need to define function overloads
because types are not enforced.
You don't need to know what code should be
accessible from where
because public/private is not a concept.
In short,
Python places fewer restrictions
on what you do,
which makes it a great environment
in which to hack and make and test and build.
In Python, you spend more time thinking
about the problem
and less time thinking about the code.

Python's hackability also makes it great
for open-source software development
(another stand-out winner of the previous ten years)
because it is so approachable.
More structured languages
like C++
add so much over head that software
written in it
can be complex to even install,
let alone navigate around the codebase,
which can make contributing to a new open-source community
an intimidating prospect.
Open-source in Python has lead to the development
of powerful,
life-saving packages like NumPy,
Matplotlib
and Pandas.
These packages form a hugely vibrant ecosystem
that has attracted users to Python for all use-cases.
The home of scientific computing,
machine learning, statistics,
visualisation and more is all in Python,
and all of that would not be possible
without Python's hackability.

It is likely that the dominant language of 2030 already exists.
The first public release of Python was in the 1990s,
but it didn't take off until twenty years later.
There are many up-and-coming languages,
such as Rust and Go,
about which I admittedly know very little,
and I'm sure that each has proponents
who could make a compelling case for why their particular pet language
will be the one to dethrone the king
But these languages solve different problems to Python.
If our needs don't change,
the only way to beat Python will be
to be a better Python.
There are two languages which I see as muscling-in
on Python's territory:
Swift and Julia.

Swift, developed by Apple,
was originally designed to replace Objective-C
as the language of iPhone app development.
However,
it's been adopted in a limited but influencial way in the machine learning community,
well outside the language's original remit:
The Tensorflow team have developed a Swift port
and FastAI have made Swift a first-class language.
Swift's main draw is that it has a clean,
highly Pythonic syntax and structure
but with additional features taken from "high-performance" languages,
such as structs, protocols, static typing (sometimes implicit) and constants.
Code can be scripted interactively
but also compiled for "C-like" speeds.
Swift's mobile device and C interoperability is a huge advantage.
Computation will become increasingly distributed
in the coming years
and software will have to run on many different hardwares.
Developing in a language which can run just as well on a beefy server
as it can on a smart-watch will slice development times.

The problems I've found when developing in Swift
isn't in getting to grips with the new features Swift introduces compared to Python.
Rather, it's in overcoming habits
deeply ingrained by years of Python development
in areas where Swift slightly deviates.
For example, in Swift you must declare a variable as either mutable
(with the "var" prefix)
or immutable
("let" - a constant).
This additional red-tape is thin,
but over many thousands of lines of code the additional time it takes
(not in typing, but remembering to do so and deciding which one to use)
could compound to become a noticeable impediment.
Even if a developer rewired the process in their brain for creating a new variable
(it probably wouldn't take long),
it's unnecessary guff for somebody trying to hack.
When you're trying something out, do you always know if a value will need to be constant or not?
When developing at pace, will a hacker not default to using "var" for everything,
especially as converting an incorrect "let" to a "var"
will take them completely out of their flow?
In which case, the feature may as well not exist.
I'm sure there is a very sensible architectural argument
for why variables couldn't be implicitly assumed to be mutable,
as is the case in C++,
but having more Pythonic defaults such as that would be a huge boost to Swift's hackability.

Both Julia and Swift exhalt their speed credentials,
but do we even need our languages to get faster?
If Moore's law holds (1),
in ten years our computers will be roughly 30x faster than they are today.
Python rose to the top despite the relatively lethargic computers of the 2010s,
so why would speed become an problem to a language after we can achieve more using it?

One reason is that Python's strong scientific,
open-source ecosystem and beginner-friendly style has attracted uses for which it was never designed.
Astrophysics and oceanography simulations all over the world are run on Python
because for many scientists the reduction in burden on their development time
is more than worth the increase in burden on the computational server's time.
If I wanted to help one of these languages to depose Python,
I would develop support libraries for use-cases which are pushing Python to its limits.
Building fervent support among a niche group is a battle-tested tactic:
languages like R and F still exist only
because some academic statisticians refuse to learn anything else.

Another reason could be that we begin to demand more from our software.
The history of the 2010s is pockmarked by privacy issues:
Bitcoin, Edward Snowden, end-to-end encrypted apps, Cambridge Analytica.
Technically-minded people have become noticeably more privacy-conscious in recent years
and there appears to be a shift among the wider population as well (2).
Recent advancements in technologies
like homomorphic encryption
and secure multi-party computation (SMPC)
provide us with the opportunity to move all off-device computation to a protected,
encrypted setting.
But this private, new world comes with a heavy computation cost
and presents a step-change in how we compute information.
If public demand for privacy comes quickly,
we may be required to adopt faster languages in the short-term
before hardware catches up.

But what if we don't like any of these languages
and instead want to develop our own?
What features might we want to implement to offer something new?
To answer this,
consider what uses have recently come fashionable
but are yet underserved by existing languages.

The last ten years have been the age of machine learning,
but very few languages offer useful solutions for implementing neural networks.
In Python, there are several competing libraries for doing this,
which makes reproducibility harder
and converting from one format to the other
can be challenging and bug-inducing.
Machine learning is slowly pervading through industry,
so it is highly likely it will be
a permanent fixture of programming
in the 2030s.
We don't rely on third-party libraries
to implement object-oriented design,
so why should we rely on them to implement neural networks?

For applications in which data travels through "classical" control structures
and predictive models many times,
running inference on trained models and online learning of models currently requires
several bespoke tools and processes
to manage effectively.
At present,
sending a computation graph
from one location to another,
as happens in federated learning,
currently requires
very clever,
hacky code.
Having differentiable objects by default
could markedly simplify
the integration of machine learning into software
and make federated learning as easy
as on-device machine learning is today.

While such a language is an interesting enough challenge to be made a reality,
I cannot see a demand for it great enough
to overtake the likes of Python.
In fact,
I think on balance Python will remain
the dominant language over the next decade.
It's a dull conclusion,
I know,
but Python's popularity is still growing in several domains
and the growing inertia in open-source libraries will only
make it more difficult
for people adopt a new language
in the short term.

**Footnotes**

1. AFAIK, there is evidence to say it's slowing down but not enough to make a definitive statement
2. At time of writing (Jan 2021),
Signal has had a huge boost in membership
due to a change
in WhatsApp's data sharing policy

[hundred-year]: http://www.paulgraham.com/hundred.html
