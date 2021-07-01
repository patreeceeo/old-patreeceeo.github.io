---
layout: post
title:  "seeing puzzleland"
date:   2021-06-30 11:11:11 -0700
categories: puzzles math
---

I picked up a used book the other day, a book of Alice in Wonderland-themed puzzles[^1], and have been working my way through it. At first I struggled to solve them without peeking at the solutions in the back, but then I made a couple of realizations.

Being a visual person, I found drawing pictures to be helpful. Gradually I developed a system, my own[^2] notation, which allowed me to capture all the information in the puzzle in a way that I find easier to analyze than the original text.

The other realization was that there's a basic algorithm to solving these puzzles. There are only a handful of permutations of the unknowns in a given problem, so the puzzler can simply brute-force try them all, reject the impossible, and whatever remains must be the solution(s).

To give a concrete example, in one puzzles we're given that, in Wonderland, unlike ours, every sane person's beliefs are 100% true, and every mad person's beliefs are 100% false. We're also given that the Mad Hatter believes that the March Hare does _not_ believe that he, the hatter and the Dormouse are all sane. Also, the Dormouse believes that the March Hare is sane.

Applying my visualization scheme to the above, I get something like:

![a directed edge-vertex graph](/alice-in-puzzle-land-graph.png)

Where "S" stands for Sane, "B" for believes, and unlabled edges simply mean "is". I used a prime operator (') to distinguish between different instances of the same noun (i.e. the hatter, hare, and mouse) for the sake of the graphing software which would otherwise make only one vertex per unique string. Finally, "~" means not, so "~B" means "does not believe."

Once I had this in place, it was fairly easy to say to myself things like "let's suppose the hatter is sane" then follow the implications using the graph as a thinking aid and find the solution. Namely, that ---

___[Spoiler] Scroll down for solution___
{: .vertical-space_full-screen}

--- They're all mad! The cat was right.

[^1]: Alice in Puzzleland, Raymond Smullyan
[^2]: At least, I believe I came up with it on my own.
