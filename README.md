# legendary

While there is an inordinate amount of wonderful content to be consumed on the internet (my addiction is HackerNews), every once in a while I get to read a legendary post that simply allows me to level up as a person. 

This is a curated list of such articles (soft limit 100):

- [What is functional programming all about](http://www.lihaoyi.com/post/WhatsFunctionalProgrammingAllAbout.html), The core of Functional Programming is thinking about data-flow rather than control-flow
- [Web design in 4 minutes](http://jgthms.com/web-design-in-4-minutes/), A very very basic css styling walkthrough!
- [React 16 migration engineering](https://code.facebook.com/posts/1716776591680069/react-16-a-look-inside-an-api-compatible-rewrite-of-our-frontend-ui-library/), brilliant take on migration engineering, illustrates the use of:
  - feature toggles to reduce merge conflicts
  - TDD for api coverage
  - regression logging for faster feedback loop
  - coverage chart for motivation
  - staggered rollout and A/B testing with an eye on product metrics for migration issues
- [Things you should never do - Joel Spolsky](https://www.joelonsoftware.com/2000/04/06/things-you-should-never-do-part-i/), Never re-write anything from "scratch", code does not rust, you will be thowing away a lot domain knowledge and bug fixes - try to incrementally refactor the codebase
- [Strategy Letter V - Joel Spolsky](https://www.joelonsoftware.com/2002/06/12/strategy-letter-v/), Micro economics 101, try to commoditize your products complement so that the demand for your product goes up:
  - Microsoft makes a free browser so that more people by it's operating system, 
  - Google makes software so that more people rely on it to feed it information which it can use for better search results which leads to them getting the lions share of advertising money (this example was added by me)
  - Note that it is easier for software to commoditize hardware than the other way around
- [Floating point visually explained](http://fabiensanglard.net/floating_point_visually_explained/), In the C language, floats are 32 bits container following the IEEE 754 standard. Their purpose is to store and allow operations on approximation of real numbers. The 32 bits are divided in three sections:
  - 1 bit S for the sign
  - 8 bits E for the exponent
  - 23 bits for the mantissa

Instead of Exponent, think of a Window between two consecutive power of two integers. Instead of a Mantissa, think of an Offset within that window. The window tells within which two consecutive power-of-two the number will be: [0.5,1], [1,2], [2,4], [4,8] and so on (up to [21272127,21282128]. The offset divides the window in 223=8388608223=8388608 buckets. With the window and the offset you can approximate a number. The window is an excellent mechanism to protect from overflowing. Once you have reached the maximum in a window (e.g [2,4]), you can "float" it right and represent the number within the next window (e.g [4,8]). It only costs a little bit of precision since the window becomes twice as large.
- [The earth is flat](https://bartoszmilewski.com/2018/01/11/the-earth-is-flat/), The scientific method has been tremendously successful in explaining the workings of our world. It led to exponential expansion of science and technology that started in the 19th century and continues to this day. We are so used to its successes that we are betting the future of humanity on it. Usually when somebody attacks the scientific method, they are coming from the background of obscurantism. Such attacks are easily rebuffed or dismissed. What I’m arguing is that science is not a property of the Universe, but rather a construct of our limited brains. We have developed some very sophisticated tools to create models of the Universe based on the principle of composition. Mathematics is the study of various ways of composing things and physics is applied composition. There is no guarantee, however, that the Universe is decomposable. Assuming that would be tantamount to postulating that its structure revolves around human brains, just like we used to believe that the Universe revolves around Earth.


The following is snippets of useful information (condensed from articles similar to the above which didn't make the cut):

- Wealth is not finite - creation of wealth is independent of the money supply. If you make a gift for someone using stones arranged in the shape of a heart, you have created something desirable and hence you are the more wealthier for it.
- "A good scientist, in other words, does not merely ignore conventional wisdom, but makes a special effort to break it. Scientists go looking for trouble. This should be the m.o. of any scholar, but scientists seem much more willing to look under rocks." - Paul Graham

