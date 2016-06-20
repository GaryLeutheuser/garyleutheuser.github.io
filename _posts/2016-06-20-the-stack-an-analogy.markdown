---
layout: post
title:  "The Stack: An Analogy"
date:   2016-06-20 9:37:00 -0400
categories: ['data structures', 'stack']
---

The stack is a wonderfully simple data structure. The essential organization of it can be imagined simply by interpreting the name as you would in everyday conversation!

The elements of this structure "stack" on top of one another like pancakes. Ethereal and intangible pancakes that exist only in your mind, but pancakes all the same.

![Stack diagram]({{ site.url }}/assets/stack.png)

Mmm, how mentally delicious! So, what can we do with this stack of pancakes? You might be thinking that you're going to cut them up and eat them - but hold on for a second. These pancakes aren't physical - they are immune to your sharp intent. So, you can't cut them. What order would you eat them in then?

While some might prefer the challenge of removing some sandwiched pancake without touching the others - I think we can agree that the most straightforward cake is the one on the very top of the stack. Indeed, the top of the stack is the point where all the action takes place. Here's the actions that are possible:

1. Place an additional pancake on top of the stack.
2. Remove the top pancake from the stack.

That's it! These are the fundamental maneuvers of stacks. This leads right into a very natural question: why would we ever want to arrange our pancakes like this? Since the analogy breaks down a bit here, I'm just going to continue using it and hope for the best.

1. <s>Stacking pancakes trades off horizontal space for vertical space.</s>
2. <s>Stacked pancakes are cut all at once instead of one at a time.</s>
3. We only care about interacting with the top pancake at any given time.

This isn't a very satisfying answer, yet. So let's examine some cases where only interacting with the most recently stacked object is useful.

One that I've just recently encountered, and is quite lovely, is the use of stacks in an iterative [depth-first search] implementation. It also has an absolutely breadthtaking symmetry with the use of queues in an iterative [breadth-first search].

Here's a description of the algorithm:

1. Place the starting [vertex] in a stack.
2. Pop a vertex from the stack, and process it.
3. Place the adjacent vertices of that vertex onto the stack.
4. Repeat from 2. Terminate when the stack is empty.

And that's it. Now, I'll leave it up to you to convince yourself that the minimal functionality of the stack makes it a very elegant data structure to use here. Certainly you could add and remove elements from an `ArrayList` in `Java`, or use some other interesting structure that supports more functionality, but I think you'll find that anything more than a stack is dead weight. And even if the dead weight doesn't quantifiably affect the program, it just doesn't seem as beautiful to me.

[depth-first search]: https://en.wikipedia.org/wiki/Depth-first_search
[breadth-first search]: https://en.wikipedia.org/wiki/Breadth-first_search
[vertex]:https://en.wikipedia.org/wiki/Graph_theory
