---
layout: post
title: "Technical Blog | Ruby Classes"
post_title: "Classy Crash Course"
post_subtitle: "Ruby Classes as Real-World Objects"
date: 2015-05-10
categories: blog technical
---

<p>
   Greetings, dear readers. As many of you know, I'm learning Ruby, one of many programming languages. Ruby is an object-oriented language, which doesn't mean much if you don't know what an object is in terms of programming. So let's talk about it. An <b>object</b> is just a thing. Any thing. Objects are the nouns of a programming language. A <b>method</b> is what objects do; methods are the verbs. Just like a person walks or a bird flies, an object <i>does</i> a method. It is important to note that not all objects can perform all methods. For instance, a person cannot fly (at least not without the assistance of some other object), but a bird can. So how does a program keep track of which objects can perform which methods? Enter: the class.
</p>
<h3>A Classy Example</h3>
<p>
  A <b>class</b> creates objects, which we call instances of that class. Each time we create a new object, we say that it is <i>instantiated</i>; this is the most important function of the class. The class also contains the definitions of the methods these objects can perform. Let's look at an example of some real-world objects and describe how they would behave if they were objects of a class. In case you don't know yet, I love to crochet. So for now, we will focus on crochet hooks as our objects.
</p>
<pre><img width="100%" src="/imgs/hook-class-1.png" /></pre>
<p>
  In Ruby, our classes are capitalized, while the objects themselves are lowercase. So we will call our example the <code>Hook</code> class. Crochet hooks come in various sizes and colors. Although the color may not be the most important attribute, it can sometimes help us to differentiate between different hooks. Much more importantly, different crochet patterns call for different hook sizes. So, each instance of the <code>Hook</code> class, will have a size and color associated with it; these will be our instance variables. Every time we instantiate a new <code>hook</code> object, it must be assigned both a size and a color. We indicate our instance variables with an <code>@</code> symbol, like this:
  <pre><img width="100%" src="/imgs/hook-class-2.png" /></pre>
  If we want to access this information regarding our <code>hook</code> object, we will need methods for this. Fittingly, we will call these methods <code>size</code> and <code>color</code>. Just for fun, let's also create a method that will give us both attributes at once; we'll call it the <code>show_hook</code> method.
  <pre><img width="100%" src="/imgs/hook-class-3.png" /></pre>
</p>
<p>
  Yikes! That seems like a lot of methods just to inspect our object. There is a shortcut for creating those first two methods, which will also allow us to access these instance variables from <i>outside</i> the class. For example, if we create a <code>Yarn</code> class, a given <code>yarn</code> object could read the <code>@size</code> and <code>@color</code> variables from a <code>hook</code> object. In order to accomplish this, we will create an attribute reader (<code>attr_reader</code>). An <code>attr_reader</code> will return the instance variable. There are also attribute writers (<code>attr_writer</code>), which allow objects outside the class to overwrite these variables. Finally, attribute accessors (<code>attr_accessor</code>) perform both functions. It will be important that these variables and the others we will create stay <i>inside</i> of the class; we don't want them to be manipulatable by anything outside of our <code>Hook</code> class. Once our blanket is made, no one should be able to alter the number of loops in a stitch or the number of stitches that have been made. (For the sake of our metaphor, let's pretend that there's no such thing as scissors or creatively destructive children). Since we do not want other objects to be able to overwrite our variable values for <code>@size</code> or <code>@color</code>, let's stick to the <code>attr_reader</code>:
  <pre><img width="100%" src="/imgs/hook-class-4.png" /></pre>
  Notice that we used symbols for our attribute readers, which we indicate with a colon at the beginning of the word. Also, our <code>size</code> and <code>color</code> methods are no longer needed. Assigning our attribute readers comes with these methods automatically. Thanks, Ruby!
</p>
<h3>More Methods</h3>
<p>
  As we have mentioned, our class should contain all of the methods a crochet hook needs to be able to carry out. So let's talk about what a crochet hook actually does. Perhaps we want to be able to write a program that can make a blanket. The hook will need to be able to complete various types of stitches. But how can we differentiate between the various types of stitches? Each stitch is made up of three actions: <code>insert</code>s, <code>yarn_over</code>s (yo), and <code>draw_through</code>s. Normally, we would create methods for each of these, but for the sake of time, I will just name each one as a <code>String</code> variable (which we indicate with quotation marks). Each stitch will be an <code>Array</code> (indicated with square brackets), containing the various action strings in a particular order. For example, let's try the single crochet stitch shown below:
  <pre><img width="40%" src="/imgs/single-crochet.png" /></pre>
  A <code>single_crochet</code> method would require one <code>insert</code>, one <code>yarn_over</code>, one <code>draw_through</code>, another <code>yarn_over</code>, and then two <code>draw_through</code>s.
  <pre><img width="100%" src="/imgs/hook-class-5.png" /></pre>
  We also might want to build in a way to create multiple stitches in a row. We can have our <code>single_crochet</code> method accept an argument that gives the number of stitches. Just to be safe, let's set the default to 1, so if we don't pass an argument, only one stitch is created.
  <pre><img width="100%" src="/imgs/hook-class-6.png" /></pre>
</p>
<p>
  Once we have all of our methods defined in the class, we are ready to create objects and ask them to carry out methods. So let's work on making our blanket! First things first: we must instantiate (create) a new <code>hook</code> object. This one will have a size of <code>"F"</code> and the color <code>"green"</code>. From there, we can ask our <code>hook</code> object to carry out any of the methods defined in the <code>Hook</code> class. Let's call our <code>show_hook</code> method to make sure things have been set up correctly. Finally, we'll carry out 20 single crochet stitches using our <code>single_crochet</code> method.
  <pre><img width="100%" src="/imgs/hook-class-7.png" /></pre>
  If we typed these commands into our Terminal, the console would looks something like this:
  <pre><img width="100%" src="/imgs/hook-class-8.png" /></pre>
</p>
<p>
  With the right methods called in the right order, we'll end up with a beautiful blanket. And since I'm sure you've all been wondering, here is the first pattern I ever designed myself:
  <pre><img width="100%" id="blanket" src="/imgs/onayemi-blanket-1.png" /></pre>
  All this with a single <code>hook</code> object performing its pre-defined methods.
</p>
<p>
  P.S. My maiden name is Onayemi, and I made this blanket for a family member with the same surname.
</p>