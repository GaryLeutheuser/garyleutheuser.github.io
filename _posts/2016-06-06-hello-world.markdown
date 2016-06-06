---
layout: post
title:  "Hello, world!"
date:   2016-06-06 14:54:38 -0400
categories: jekyll update
---
For this blog's first post, I've decided to do a spin on the classic ["Hello, world!"] programming exercise. For those that are unfamiliar, such a program has one simple goal: print the text "Hello, world!" to the screen. It's a nice little [sanity check] when you're getting to grips with a new language or environment (or perhaps a blog [;) )].



Right now, I know 4 programming languages: `Java`, `C`, `JavaScript`, and `C++`. Or, I at least know enough of them to where I'm comfortable creating a very simple program in them. That's basically expertise, right?

# Java
{% highlight java %}
public class HelloWorld {
  public static void main(String [] args) {
    System.out.println("Hello, world!");
  }
}
{% endhighlight %}

`Java` is definitely the most verbose of the group. Imagine it went to a party:

> Javandine: Of the standard greetings, I bid thee 'Hello'. I will now try to perform the procedure for acquiring your identifier, human. What is your 'name'?   
John: Uhm, it's John?

I have to say, in many ways, I quite like Java's verbosity. It gives me a feeling of structure, communication, and solidity. This is in stark contrast to when I take a look at, say, a snippet in `APL` (this one [apparently] sorts words stored in a matrix `X` by length):

{% highlight APL %}
X[⍋X+.≠' ';]
{% endhighlight %}

... this gives me an overwhelming sense of cleverness, density, and wonder. It feels like I'm reading a short poem, like this one by Emily Dickinson:

> The show is not the show,  
But they that go.  
Menagerie to me  
My neighbor be.  
Fair play &mdash;  
Both went to see.

Both ideas are really quite lovely: that of clear, verbose expression for the purposes of easing communication, and masterfully and carefully reducing ideas to minimalistic forms resulting in very short code (or poetry).

# C
{% highlight c %}
#include <stdio.h>

int main(void) {
  printf("Hello, world!\n");
  return 1;
}
{% endhighlight %}

This is probably very close to the very first program I ever wrote, since `C` was the first programming language I was exposed to. I don't write a lot of `C` these days, but when I do, I usually end up with a segmentation fault.

# JavaScript
{% highlight javascript %}
console.log("Hello, world!");
{% endhighlight %}

If you are so inclined as to want to run this useful bit of code, your browser probably has a `JavaScript` console where you can do so (and lay eyes on the output that you definitely didn't see coming!). In Chrome, you can use the key combo `ctrl-shift-j` to pop open the console.

# C++
{% highlight c++ %}
#include <iostream>

int main(void) {
  std::cout << "Hello, world!" << std::endl;
}
{% endhighlight %}

`C++` is the language that I practice and use the least of these 4, since my school pretty much exclusively uses `Java` in its object-oriented curriculum. Almost all of my knowledge of the language comes from trekking through the first few chapters of [Accelerated C++]. One of the things I find interesting about the languane is the existence of `namespace`s.

My (limited) understanding of the `namespace` is that it prevents ambiguity - by specifying _which_ 'thing' you are referring to - because potentially, there's more than one. In this case, `std` is the namespace that contains the versions of `cout` and `endl` that I'm using.

I'd like to illustrate some sort of tangible situation where such an idea is necessary.

I personally have a few friends named Alex, and to differentiate between them when addressing them, there's a few techniques my friends and I use:

* Simply ignore the difference and call them both Alex - my personal favorite
* Use their last name (either Alex Lastname or just Lastname)
* Hope that the context is clear enough for them to differentiate
* Physically clarifying (pointing, nodding head toward one of them, etc.)

Of course, these issues only arise when both Alex's are present simultaneously. You know, I would actually like to see a language that performs solution one, and just have it simply guess between all the different meanings something could have. It would be critical, too, that it never tell the programmer which one it decided on.

Imagine how adventurous writing code in that language would feel!

["Hello, world!"]: https://en.wikipedia.org/wiki/%22Hello,_World!%22_program
[sanity check]: https://en.wikipedia.org/wiki/Sanity_check
[;) )]: https://xkcd.com/541/
[apparently]: https://en.wikipedia.org/wiki/APL_(programming_language)#Sorting
[Accelerated C++]: http://www.amazon.com/Accelerated-C-Practical-Programming-Example/dp/020170353X
