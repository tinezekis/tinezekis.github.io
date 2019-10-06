---
layout: post
title: "Technical Blog | Object-Oriented Programming"
post_title: "Acting as Individuals and as a Group"
post_subtitle: "Instance Methods vs. Class Methods"
date: 2015-05-17
categories: blog technical
---

<p>
  When we create a class in Ruby, we are able to create several instances of that class (objects). As we have discussed in <a target="_blank" href="{{ page.previous.url | prepend: site.baseurl | replace: '//', '/' }}">a previous post</a>, objects, or instances of a class, are the nouns of an Object-Oriented Programming (OOP) language. And if the objects are the nouns, then methods are the verbs. Methods, are the focus of this post: we will discuss the difference between instance methods and class methods.
</p>
<p>
  As you may have guessed, instance methods get performed on an individual instance of the class, whereas class methods are performed on all instances of the class (the class as a whole). In order to illustrate this difference, let us consider the example of a <code>Car</code> class. Each <code>car</code>, an instance of the <code>Car</code> class, will have its own attributes, which are called instance variables. Let us say that our instances are distinguished by make, model, color, and year:
  <pre><img width="100%" src="/imgs/car-class-1.png" /></pre>
</p>
<p>
  My first car was an emerald green '98 Honda Accord. I loved that car. So in honor of her, we will name our instance <code>my_first_car</code>. My current car is a black '99 Honda Civic. It is much less accomplished, but it deserves its own instance nonetheless, I suppose. So here are out two instances:
  <pre><img width="100%" src="/imgs/car-class-2.png" /></pre>
</p>
<p>
  So now that we have a couple of cars to talk about, let's have them do things. First, let's create a couple of methods: one that will drive the car, and one that will tell us the mileage on each car. What kind of methods do you think we'll need for these tasks? Well, the mileage will not be the same for both cars, and we certainly won't be driving them in one go. So each instance of the <code>Car</code> class will need to perform these methods for itself. Thus, we will need <i>instance</i> methods:
  <pre><img width="100%" src="/imgs/car-class-3.png" /></pre>
  In this case, calling the <code>drive</code> method on <code>my_first_car</code> will add 50 miles to the total <code>@mileage</code> and print
  <pre><samp>=> You drove 50 miles in your Honda Accord.</samp></pre>
  to the console. Calling the <code>odometer</code> method on <code>my_current_car</code> will return the <code>@mileage</code> that is currently on the Honda Civic and print
  <pre><samp>=> The Honda Civic has 0 miles on it.</samp></pre>
  to the console.
</p>
<p>
  But what if we want a way to compare the mileage on both cars? This will be quite impossible with an instance method because one car does not know the mileage of another car. Here's where we need a <i>class</i> method. Let's start by introducing some class variables that will store the information we need: <code>@@most_mileage</code>, <code>@@make_with_most</code>, and <code>@@model_with_most</code>. Next, we will want to introduce the points during which we will need to check for which car is currently the one with the most mileage. That will look something like this:
  <pre><img width="100%" src="/imgs/car-class-4.png" /></pre>
  Now, let's define what happens each time we check for which car currently has the most mileage, as well as what happens when we call the <code>most_mileage</code> class method:
  <pre><img width="100%" src="/imgs/car-class-5.png" /></pre>
</p>
<p>
  Let's say that <code>my_current_car</code> has 75,000 miles on it. But <code>my_first_car</code> had 200,000 miles on it (and still ran like it was brand new!). Here's what it will look like for us to call the <code>most_mileage</code> method as well as the message that would be printed to the console:
  <pre><code>Car.most_mileage</code></pre>
  <pre><samp>=> The Honda Accord has the most mileage with 200000 miles...and counting!</samp></pre>
  This method has successfully compared all existing instances of the <code>Car</code> class and told us which one has the most mileage.
</p>
<p>
  So here are the major takeaways I hope you have gained from this post:
  <ol>
    <li>Instance methods act on one particular instance of a class.</li>
    <li>Class methods act on all existing instances of the class at once</li>
    <li>My first car was glorious and had over 200,000 miles on it before it was sadly totaled.</li>
  </ol>
  'Tine out.
</p>
<p>
   <h4>Resources:</h4>
   <ul>
    <li><a target="_blank" href="http://www.railstips.org/blog/archives/2009/05/11/class-and-instance-methods-in-ruby/">RailsTips: Class and Instance Methods in Ruby</a></li>
    <li><a target="_blank" href="http://ruby-doc.org/core-2.2.0/doc/syntax/calling_methods_rdoc.html">Ruby-Doc.org: Calling Methods</a></li>
    <li><a target="_blank" href="http://ruby-doc.org/core-2.2.0/doc/syntax/methods_rdoc.html">Ruby-Doc.org: Methods</a></li>
   </ul>
</p>
