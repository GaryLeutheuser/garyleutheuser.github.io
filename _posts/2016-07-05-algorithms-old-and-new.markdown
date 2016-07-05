---
layout: post
title:  "Old Algorithms"
date:   2016-07-05 11:54:00 -0400
categories: ['history', 'algorithm']
---

According to a quick Google search, the [Euclidean algorithm] is "one of the oldest algorithms in common use". Here's a little time line I've pulled from the information in the Wikipedia entry:

1. Euclidean algorithm discovered by someone, somewhere.
2. 300 BC - Appears in Euclid's *Elements*.
3. Independent discovery in India and China.
4. ~500 - [Aryabhata] calls it the "pulverizer[^1]".
5. 1624 - Found in *Pleasant and enjoyable problems*. First time in Europe.

In addition to this impressive history, there's also this quote from Donald Knuth featured in the article:

>"[The Euclidean algorithm] is the granddaddy of all algorithms, because it is the oldest nontrivial algorithm that has survived to the present day."

All in all, this was a pretty grand success for Google and Wikipedia - the first link appears to have led me directly to the answer that I asked.

What about the "most modern" algorithm?

This is harder for 2 reasons: 1) The current bleeding edge of research will take ages to sink into the general knowledge pool (if it ever will), so I don't understand any of it at a glance, and 2) there's a *lot* of information available, from image stitching, to computer vision, cryptography, etc.

There are some pretty neat and relatively new algorithms I've learned about in class recently, though. Here's a nice little list, with the dates being pulled from Wikipedia.

* 1930s: [Prim's]: Finds a minimum spanning tree for a weighted undirected graph.
* 1940s: [Binary search]: Searches an array for an element.
* 1940s: [Merge sort]: Sorts an array.
* 1950s: [Breadth-first search]: Graph traversal / maze solving.
* 1950s: [Bellman-Ford]: Solves [single-source shortest paths].
* 1950s: [Dijkstra's]: Solves [single-source shortest paths].
* 1960s: [Kahn's]: Finds a topological sort of a directed graph.
* 1970s?: [Kadane's]: Solves the [maximum subarray problem].

[^1]: I think from now on, I'll refer to algorithms by names I would expect to hear on BattleBots.

[Euclidean algorithm]: https://en.wikipedia.org/wiki/Euclidean_algorithm
[Aryabhata]: https://en.wikipedia.org/wiki/Aryabhata
[Prim's]: https://en.wikipedia.org/wiki/Prim%27s_algorithm
[Binary search]: https://en.wikipedia.org/wiki/Binary_search_algorithm
[Merge sort]: https://en.wikipedia.org/wiki/Merge_sort
[Breadth-first search]: https://en.wikipedia.org/wiki/Breadth-first_search
[Bellman-Ford]: https://en.wikipedia.org/wiki/Bellman%E2%80%93Ford_algorithm
[Dijkstra's]: https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm
[Kahn's]: https://en.wikipedia.org/wiki/Topological_sorting#Kahn.27s_algorithm
[Kadane's]: https://en.wikipedia.org/wiki/Maximum_subarray_problem#Kadane.27s_algorithm
[single-source shortest paths]: https://en.wikipedia.org/wiki/Shortest_path_problem#Single-source_shortest_paths
[maximum subarray problem]: https://en.wikipedia.org/wiki/Maximum_subarray_problem
