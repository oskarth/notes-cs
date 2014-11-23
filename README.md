# Notes on Computer Science

Broad subject, but this is an umbrella repository for my notes on
CS. To start with, papers from HS paper of the week, papers relevant
to my work, and papers from papers we love.

In short: papers and books on CS.

## Paper of the week, courtesy of HS

Basic premise is that papers have a lot of good stuff, but hard to
find the right ones. By crowdsourcing and focusing the HS community,
people can read important papers and find venues to discuss them.

Let's put it this way: there's a big difference between programmers
who read papers/textbooks and the ones who don't. If you want to be
good, do it right. Read papers.

### Growing a Language (1998), by Steele

Starts with a fundamental question: should a programming language be
small or large? In the sense of vocabulary. Trade-off: long time to
learn vs hard to use. Is that a real trade-off?

As programmers we have to define "words" like max, a concept which is
evident to most people.

Designing not a small language, nor a big one. One that can grow
(i.e. change for the better).

Comparing APL to Lisp, in favor of Lisp: Grown by users, not just
creator. In Lisp, new words defined by users looks and works like
primitives.

Exercise: defining garbage collection in terms of one syllable words.

> Our main goal in designing a language should be to plan for growth.

How to grow? Make it organic, fast for people change things. Should
feel like primitives.

> A good programmer in these days does not just write programs. A good
> programmer builds a working vocabulary. In other words, a good
> programmer does language design, though not from scratch, but by
> building of a base language.

Reminds me of Shakespeare - it's not about words per se, it's about
vocabulary. How you piece things together.

Meta point: he started from a base language of just words of one
syllable, and then added a bunch of words with definitions, and some
rules, such as adding "ing" means it's a person doing something,
etc. Makes for a very lucid and easy to understand text. Reference to
Basic English by Ogden.

To write a program of big size requires the definition of hundreds of
new words. Steele says it can't be done any other way. _Maybe_ you can
use a big, complex language which has solved all these things.

Similar to pg and his view of getting good at Lisp hacking - making
embedded languages / DSLs.

Choose short words when you can.

He thinks it's a good idea to only use words of one syllable and
define terms. Inclined to agree.

### Queue

See
https://www.hackerschool.com/blog/42-paper-of-the-week-reflections-on-trusting-trust
and https://www.hackerschool.com/blog


(Reflections on Trusting
Trust)[https://www.ece.cmu.edu/~ganger/712.fall02/papers/p761-thompson.pdf]

(Worlds: Controlling th Scope of Side Effects)[http://www.vpri.org/pdf/tr2011001_final_worlds.pdf]

and more.

(The Power of Two Random Choices: A Survey of Techniques and
Results)[http://www.eecs.harvard.edu/~michaelm/postscripts/handbook2001.pdf]
