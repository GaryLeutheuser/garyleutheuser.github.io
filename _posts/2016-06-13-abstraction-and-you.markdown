---
layout: post
title:  "Abstraction and You"
date:   2016-06-13 11:22:00 -0400
categories: abstraction java language
---
Take a moment and think about the journey a computer program goes through on its way to running on your computer. It might look something like this:

1. High level code (usually you would write this part yourself)
2. Compiler translates high level code to assembly
3. Assembler translates assembly to machine code

The name of the game here is abstraction. How much detail is important, and how much of it do we want to carefully ignore? While coding, a lot of time is generally spent at a very high level of abstraction. Take a look at this Java code:

{% highlight java %}
import java.util.ArrayList;

public class Test {
  public static void main(String [] args) {
    ArrayList<String> strings = new ArrayList<String>();
    strings.add("a string");
  }
}
{% endhighlight %}

This is doing a lot of work in only two lines: we've allocated some space for this fancy dynamically sized data structure, consisting of strings of varying length, and added a string to it without even breaking a sweat! (Well, you might have started sweating in excitement over how quickly this can be accomplished.)

Now, using `javap -c Test` (`javap` is "The Java Class File Disassembler"), let's take a look at the disassembled code.

{% highlight assembly %}
Compiled from "Test.java"
public class Test {
  public Test();
    Code:
       0: aload_0       
       1: invokespecial #1                  // Method java/lang/Object."<init>":()V
       4: return        

  public static void main(java.lang.String[]);
    Code:
       0: new           #2                  // class java/util/ArrayList
       3: dup           
       4: invokespecial #3                  // Method java/util/ArrayList."<init>":()V
       7: astore_1      
       8: aload_1       
       9: ldc           #4                  // String a string
      11: invokevirtual #5                  // Method java/util/ArrayList.add:(Ljava/lang/Object;)Z
      14: pop           
      15: return        
}
{% endhighlight %}

It doesn't look too bad in terms of code quantity - but it's certainly harder to read.

Now, my point is not to dredge through the disassembly, showing how the translation process works, or anything like that. What I find so fascinating is purely the difference in abstraction. We've moved away from the realm where human-readability is the most important characteristic of the code.

It's worth mentioning at this point that we could go even further: all the way to the machine code. This is the final leg of the program's journey, where no human dares tread (at least not this human!). At this point, you have a binary file (consisting of 0s and 1s)[^1] that's executable by the machine. To us, of course, it looks like a bunch of nonsense, but to the machine, it's the beautiful program that we crafted at the beginning of this discussion.

{% highlight binary %}
01110101 01100101 01101111 01100001 01110101 01100101 01101111
01100001 01100100 01110100 01110101 01100101 01101000 01101111
01110101 01110011 01101110 01100101 01101111 01101000 01110101
01100101 01100001 01101000 01110101 01100101 01110100 01100001
01110101 01101000 01110100 01100100 01110000 00101110 00101100
01110000 00001010 00101110 00101100 01100100 01101000 00100111
00001010 ...
{% endhighlight %}

What a lovely program![^2]

So, it's evident that there's a shifting that occurs over the process of creating and running a program. It shifts from human-readable to machine-readable.

While that's pretty neat (I sure think it is), I actually think the most entertaining part is considering going the other way. What I mean is instead of going to the dead end on the machine readable side (machine code), what if we went to the other side, the "extremity" of human-readability?

You might argue that we've already seen it: the Java code at the beginning of the post. And I would agree that this is the point where most people agree the abstraction should stop, at least right now. But what if it didn't?

An interesting example of increasing abstraction to a fault can be created for language. Consider a term like "refrigerator" - this one replaces "a space that makes the things inside colder". Since this was apparently such a common term, or simply too cumbersome, it's even usually shortened to "fridge". Suppose we also liked to identify the color of fridges often - maybe a white fridge would then be a "widge".

But we don't do that. At a certain point, we stop abstracting, and use what we have ("white fridge"), only carefully and slowly introducing words when necessary. This is interesting to me - it seems like it comes almost naturally to everyone. We agree to some invisible rules of language - keeping things general and the whole of communication efficient while using a reasonable amount of memory.

I like to wonder sometimes about the "widges" of programming - and whether they're beneficial or not. The human-machine relationship is a wonderfully curious thing.

[^1]: All files technically already consist of 0s and 1s, but in this one, the 0s and 1s are meant for the machine, not for some human-readable encoding like ASCII.

[^2]: For the detail-oriented types, this is not the actual program, just a bunch of randomness - though I certainly couldn't tell the difference :).
