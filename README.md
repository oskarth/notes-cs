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

(http://www.cs.virginia.edu/~evans/cs655/readings/steele.pdf)[link]

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

Exercise: defining garbage collection in terms of one syllable
words. Here's how Tom Ballinger did it:
(http://ballingt.com/2014/09/21/garbage-collection.html)[garbage collection].

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

### Reflections on Trusting Trust (1984), by Thompson

(https://www.ece.cmu.edu/~ganger/712.fall02/papers/p761-thompson.pdf)[link]

Starts with: to what extent should one trust a statement that a
program is free of Trojan horses?

Is this true? If it is, it's pretty amazing:

> This brings me to Dennis Ritchie. Our collaboration has been a thing
> of beauty. In the ten years that we have worked together, I can
> recall only one case of miscoordination of work. On that occassion,
> I discovered that we had both written the same 20-line assembly
> language program. I compared that sources and was astounded to find
> that they match character-for-character.

That's how constrained the design space is for great
programmers. Similar to how FP in Scala they talk about function
signatures that can only be implemented in one way. The rest is just
conventions and getting rid of fluff.

A game he used to play in college: write the shortest self-reproducing
program. I.e., when compiled and executed, it will produce an exact
copy of its source.

I read it more carefully now and it's pretty mind-blowing. The basic
concept is this: In order to add a feature to the C compiler we have
to change the source code, which is written in C. When we try to
compile something the binary compiler doesn't have support for, we
will get an error. How do we get around this problem?

He gives an example of the interpreter of character escape sequences
(\n etc). If we want to add a new one, we can first add a if(c=='v')
return(11) line (ascii decimal for \v, a vertical tab). Then it
compiles, we swap the binary and then we can write \v, which gets
interpreted correctly. We have now gone around the chicken-and-egg
problem.

A similar technique can be done maliciously. If we come upon a certain
pattern in the reading of the source code, we trigger some bug. This
is added to the source code of the compiler, then compiled into new
compiler. This might be too obvious, since it's in the source code,
but we can hide it - write a program similar to the Quine (?)
described in the beginning, and the code to prompt this bug will be
inserted. We now have a new binary, and can remove it from the source
code. There's no trace of the malicious bug triggering. This is a
Trojan horse.

The gist of it is: you have to write it yourself to trust it, or trust
the people behind the code. Many levels where this could happen - C,
assembly, hardware etc. Many security implications.

There exists some kind of work-around for this, given that you have
multiple compilers. Schneier puts it better.

https://www.schneier.com/blog/archives/2006/01/countering_trus.html
and David A. Wheleer: "Countering Trusting Trust through Diverse
Double-Compiling,"

### Error Detecting and Error Correcting Codes, by Hamming
(Error Detecting and Error Correcting Codes)[http://www.lee.eng.uerj.br/~gil/redesII/hamming.pdf]

### Queue

Read again: https://www.ece.cmu.edu/~ganger/712.fall02/papers/p761-thompson.pdf

https://www.hackerschool.com/blog/44-paper-of-the-week-error-detecting-and-error-correcting-codes

More: https://www.hackerschool.com/blog/46-paper-of-the-week-on-understanding-data-abstraction-revisited

More: https://www.hackerschool.com/blog/48-paper-of-the-week-the-power-of-interoperability-why-objects-are-inevitable

More: https://www.hackerschool.com/blog/49-paper-of-the-week-the-chubby-lock-service-for-loosely-coupled-distributed-systems

More: https://www.hackerschool.com/blog/51-paper-of-the-week-out-of-the-tar-pit

More: https://www.hackerschool.com/blog/53-paper-of-the-week-managing-update-conflicts-in-bayou-a-weakly-connected-replicated-storage-system

More: https://www.hackerschool.com/blog/55-paper-of-the-week-worlds-controlling-the-scope-of-side-effects

(Worlds: Controlling th Scope of Side Effects)[http://www.vpri.org/pdf/tr2011001_final_worlds.pdf]

More: https://www.hackerschool.com/blog/57-paper-of-the-week-the-power-of-two-random-choices-a-survey-of-techniques-and-results

(The Power of Two Random Choices: A Survey of Techniques and
Results)[http://www.eecs.harvard.edu/~michaelm/postscripts/handbook2001.pdf]


## Queue

(The Comfy 6502 compiler)[http://www.pipeline.com/~hbaker1/sigplannotices/sigcol04.pdf]
