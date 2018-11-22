# legendary

While there is an inordinate amount of wonderful content to be consumed on the internet (my addiction is HackerNews), every once in a while I get to read a legendary post that simply allows me to level up as a person.

This is a curated list of such articles (soft limit 100):

1. [Technical debt is not a debt, but an unhedged call option](https://erikbern.com/2014/12/30/everything-i-learned-about-technical-debt.html), As long as you acknowledge that you are taking on debt, it may make sense to take it on, e.g. shipping a product earlier with debt laden code will lead to a better ROI with which one could hire more resources to "repay" the debt. Note that this needs to be a very conscious decision with a fixed plan. Also, something to keep in mind - "If it ain't broke, don't fix it".

1. [System design - Job Scheduler](https://segment.com/blog/introducing-centrifuge/), A very neat article on design an event processing engine in a high fault environment. Use a write heavy database to segment jobs and a co-ordinating service to execute the jobs. The database itself consists of simple `job` and `job_state_transition` tables.

1. [What is functional programming all about](http://www.lihaoyi.com/post/WhatsFunctionalProgrammingAllAbout.html), The core of Functional Programming is thinking about data-flow rather than control-flow

1. [Web design in 4 minutes](http://jgthms.com/web-design-in-4-minutes/), A very very basic css styling walkthrough!

1. [React 16 migration engineering](https://code.facebook.com/posts/1716776591680069/react-16-a-look-inside-an-api-compatible-rewrite-of-our-frontend-ui-library/), brilliant take on migration engineering, illustrates the use of:

    - feature toggles to reduce merge conflicts
    - TDD for api coverage
    - regression logging for faster feedback loop
    - coverage chart for motivation
    - staggered rollout and A/B testing with an eye on product metrics for migration issues

1. [Things you should never do - Joel Spolsky](https://www.joelonsoftware.com/2000/04/06/things-you-should-never-do-part-i/), Never re-write anything from "scratch", code does not rust, you will be thowing away a lot domain knowledge and bug fixes - try to incrementally refactor the codebase

1. [Strategy Letter V - Joel Spolsky](https://www.joelonsoftware.com/2002/06/12/strategy-letter-v/), Micro economics 101, try to commoditize your products complement so that the demand for your product goes up:

    - Microsoft makes a free browser so that more people by it's operating system,
    - Google makes software so that more people rely on it to feed it information which it can use for better search results which leads to them getting the lions share of advertising money (this example was added by me)
    - Note that it is easier for software to commoditize hardware than the other way around

1. [Floating point visually explained](http://fabiensanglard.net/floating_point_visually_explained/), In the C language, floats are 32 bits container following the IEEE 754 standard. Their purpose is to store and allow operations on approximation of real numbers. The 32 bits are divided in three sections:

    - 1 bit S for the sign
    - 8 bits E for the exponent
    - 23 bits for the mantissa
    - Instead of Exponent, think of a Window between two consecutive power of two integers. Instead of a Mantissa, think of an Offset within that window. The window tells within which two consecutive power-of-two the number will be: [0.5,1], [1,2], [2,4], [4,8] and so on (up to [21272127,21282128]. The offset divides the window in 223=8388608223=8388608 buckets. With the window and the offset you can approximate a number. The window is an excellent mechanism to protect from overflowing. Once you have reached the maximum in a window (e.g [2,4]), you can "float" it right and represent the number within the next window (e.g [4,8]). It only costs a little bit of precision since the window becomes twice as large.

1. [The earth is flat](https://bartoszmilewski.com/2018/01/11/the-earth-is-flat/), The scientific method has been tremendously successful in explaining the workings of our world. It led to exponential expansion of science and technology that started in the 19th century and continues to this day. We are so used to its successes that we are betting the future of humanity on it. Usually when somebody attacks the scientific method, they are coming from the background of obscurantism. Such attacks are easily rebuffed or dismissed. What I’m arguing is that science is not a property of the Universe, but rather a construct of our limited brains. We have developed some very sophisticated tools to create models of the Universe based on the principle of composition. Mathematics is the study of various ways of composing things and physics is applied composition. There is no guarantee, however, that the Universe is decomposable. Assuming that would be tantamount to postulating that its structure revolves around human brains, just like we used to believe that the Universe revolves around Earth.

1. [Love your bugs](http://akaptur.com/blog/2017/11/12/love-your-bugs/), Some really interesting bugs and the attitude + mindset required for effective bugfixing.

1. [Why don’t software development methodologies work?](http://typicalprogrammer.com/why-dont-software-development-methodologies-work), Essentially, the secret to a team's success is a shared vision and effective communication. Methodologies are rather pointless if the previous does not hold true.

1. [Laws of UX](https://lawsofux.com/)
  
    1. _The time to acquire a target is a function of the distance to and size of the target_ -- Paul Fitts. E.g. if a function needs to be accessed often and/or quickly, make the button big
  
    1. _The time it takes to make a decision increases with the number and complexity of choices_ -- William Edmund Hick and Ray Hyman. E.g. only provide choices when a good default does not exist.
  
    1. _Users spend most of their time on other sites. This means that users prefer your site to work the same way as all the other sites they already know_ -- Jakob Nielsen. E.g. respect the platform’s conventions and interface guidelines.
  
    1. _People will perceive and interpret ambiguous or complex images as the simplest form possible, because it is the interpretation that requires the least cognitive effort of us_ -- Law of Prägnanz. E.g. do not stuff too much detail into a small space.
  
    1. _Objects that are near, or proximate to each other, tend to be grouped together_ -- Law of Proximity. E.g. put actions that do similar things together.
  
    1. _The average person can only keep 7 (plus or minus 2) items in their working memory_ -- George Miller. E.g. reduce the number of things your users have to remember.
  
    1. _Any task will inflate until all of the available time is spent_ -- Cyril Northcote Parkinson. E.g. make tasks short, simple and with set deadlines
  
    1. _Users have a propensity to best remember the first and last items in a series_ -- Serial Position Effect. E.g. put the important things at the beginning or at the end.
  
    1. _Tesler’s Law, also known as The Law of Conservation of Complexity, states that for any system there is a certain amount of complexity which cannot be reduced._ E.g. removing features from your product may result in users not being able to achieve some goals.
  
    1. _The Von Restorff effect, also known as The Isolation Effect, predicts that when multiple similar objects are present, the one that differs from the rest is most likely to be remembered._ E.g. make the most important thing stand out.  Alternatively: If you want to stand out from competition, find a feature which is always the same and make it different.

1. [The 3 Stages of Failure in Life and Work]( https://jamesclear.com/3-stages-of-failure )
  
    1. Stage 1 is a Failure of Tactics. These are HOW mistakes. They occur when you fail to build robust systems, forget to measure carefully, and get lazy with the details. A Failure of Tactics is a failure to execute on a good plan and a clear vision. Fixing a failure of tactics involves recording your process, measuring your outcomes (the provided example of measuring your progress at the gym hit home), and finally reviewing and adjusting your tactics.
  
    2. Stage 2 is a Failure of Strategy. These are WHAT mistakes. They occur when you follow a strategy that fails to deliver the results you want. You can know why you do the things you do and you can know how to do the work, but still choose the wrong what to make it happen. Fixing a failure of strategy involves launching it quickly, doing it cheaply and revising it rapidly (startup 101).
  
    3. Stage 3 is a Failure of Vision. These are WHY mistakes. They occur when you don't set a clear direction for yourself, follow a vision that doesn't fulfill you, or otherwise fail to understand why you do the things you do. Most importantly (and also something that resonated with me personally), fixing a failure of vision involves taking stock of your life, determining your non-negotiable and then navigating criticism!

1. [The absolute minimum every software developer must know about unicode and character sets](https://www.joelonsoftware.com/2003/10/08/the-absolute-minimum-every-software-developer-absolutely-positively-must-know-about-unicode-and-character-sets-no-excuses/), long story short there is no such thing as plain text. Unicode is a standard that defines characters as code points. Initially, there were less than 65,536 characters so it was possible to store each character using 2 bytes (16 bits). However, once the standard grew, there evolved multiple character encoding schemes: UTF-8 (where every code point from 0-127 is stored in a single byte. Only code points 128 and above are stored using 2, 3, in fact, up to 6 bytes), UTF-16, UTF-7, UTF-32, Windows-1252 (the Windows 9x standard for Western European languages), ISO-8859-1, aka Latin-1 (also useful for any Western European language). Note that the UTF encodings can also potentially have a Byte Order Mark (BOM) at the start of the string which indicates their endianess. Finally, it really only makes sense to use UTF-8 as it is the most efficient with higest compatibility :)

1. [Advanced web-security topics](https://blog.georgovassilis.com/2016/04/16/advanced-web-security-topics/)

## Classic

The following is snippets of useful information (condensed from articles similar to the above which didn't make the cut):

1. [The point of microservices](https://erikbern.com/2018/06/04/missing-the-point-about-microservices.html), is being able to deploy and test independently for rapid iteration. The article itself does not cover version management however.

1. [A road to common lisp](http://stevelosh.com/blog/2018/08/a-road-to-common-lisp/), an excellent resource on getting started with lisp - basically get SBCL and a couple of books :)

1. "Concurrency is dealing with inevitable timing-related conflicts, parallelism is avoiding unnecessary conflicts". A concurrent solution to an event handling problem uses a queue to resolve conflicts whereas a parallel solution to a computational problem avoids unnecessary conflicts: [Vending machine vs gifts](http://yosefk.com/img/n/vending-vs-gifts.png), [Parallelism and concurrency need different tools](http://yosefk.com/blog/parallelism-and-concurrency-need-different-tools.html)

1. Wealth is not finite - creation of wealth is independent of the money supply. If you make a gift for someone using stones arranged in the shape of a heart, you have created something desirable and hence you are the more wealthier for it.

1. "A good scientist, in other words, does not merely ignore conventional wisdom, but makes a special effort to break it. Scientists go looking for trouble. This should be the m.o. of any scholar, but scientists seem much more willing to look under rocks." - Paul Graham

1. [The Log: What every software engineer should know about real-time data's unifying abstraction](https://engineering.linkedin.com/distributed-systems/log-what-every-software-engineer-should-know-about-real-time-datas-unifying), use a log infrastructure like Apache kafka for distributed data consistency - a bit enterprise heavy but some neat insights.

1. [Event sourcing made simple](https://kickstarter.engineering/event-sourcing-made-simple-4a2625113224), Event sourcing is like git for data. There are generally four components that make a (minimal) Event Sourcing system: 

    1. Events: persisted and immutable.
    2. Aggregates: represent the current state of the application.
    3. Calculators: read events and update aggregates accordingly.
    4. Reactors: _react_ to events as they are created. They trigger side-effects and might create other events in turn.

1. [Stacked diffs vs. pull requests](https://jg.gg/2018/09/29/stacked-diffs-versus-pull-requests/), The basic idea of stacked diffs is that you have a local checkout of the repository which you can mangle to your heart's content. The only thing that the world needs to care about is what you want to push out for review. This means you decide what view of your local checkout the reviewers see. You present something that can be "landed" on top of master. 

    The typical workflow is to work right on top of master, committing to master as you go. For each of the commits, you then use the Phabricator command line tool to create a "Diff" which is the Phabricator equivalent of a Pull Request. Unlike Pull Requests, Diffs are usually based on exactly one commit and instead of pushing updates as additional commits, you update the single commit in place and then tell Phabricator to update the remote view. When a Diff gets reviewed and approaved, you can "land" it onto remote master. Your local copy and master don't have to be in perfect sync in order to do this. You can think of this as the remote master cherry-picking the specific commit from your git history.
